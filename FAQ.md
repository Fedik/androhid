**Why does this application need root?**

Unfortunately the android SDK does not provide a feature to add a record to the bluetooth _service discovery protocol_ server (sdp server). Normally it's not a security hole to add this record to the sdp server but the android SDK is at the moment not very mature in bluetooth features. To add the sdp record we use the linux sdptool with root permissions for now.

**Which bluetooth stacks work with AndroHid?**

  * The Linux Bluez stack is tested successfully under KUbuntu and Arch Linux.
  * The Windows bluetooth stack doesn't work at the moment.
  * The Mac OS X bluetooth stack is not tested for now. Please inform me about your results!

**Why does AndroHid not work with my Windows?**

The reason are technical issues which are described in the technical [documentation](http://code.google.com/p/androhid/wiki/AndroHid).

**How can I configure the keyboard signals sent by the different Player/Video/Presenter Tab?**

A howto can be found [here](http://code.google.com/p/androhid/wiki/Keycodes).