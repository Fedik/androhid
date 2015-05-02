### Introduction ###

Some technical issues of AndroHid will be described here, going into technical details which may not be of any interest for end users.

### Bluetooth with L2CAP ###

Android SDK does not provide any functionality for the l2cap bluetooth protocol which is required for the bluetooth HID specification. Nevertheless we can communicate with the android bluetooth stack _bluez_ directly via the _native development kit_ (NDK). Hence all bluetooth handling is done in native C code working even on android versions previous to 2.0 where for the first time bluetooth functionality was invented in the SDK.

### Service discovery protocol ###

To add the sdp record to the android sdp server the linux tool _sdptool_ is used. As dbus interaction to bluez is locked down for users we need to do this as root. This is the reason why AndroHid requires a rooted android device. Normally the HID specification provides not only keyboard but also mouse signal support. As we can't add a user defined sdp record only keyboard support is provided for now.

### L2CAP sockets ###

The bt HID standard requires the client listening on control and interrupt channel for host connection. The PSM for control is 0x11 and for interrupt is 0x13. As the android bluetooth daemon is blocking these two PSMs for no reason, AndroHid can't open listening sockets and the HID host can't connect actively to AndroHid but must wait for a reconnect from AndroHid to host which is done when the user clicks the _connect_ button in the user menu. Connecting this way to linux hosts seems to be ok, but windows hosts expect a correct listening socket (control and interrupt) on the HID client to setup before accepting remote connection by the client.