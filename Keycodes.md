### User defined keycodes ###

Although the default key mapping is a good prerequisite to let you start out of the box with AndroHid, in some cases user configuration becomes necessary. As different music players (and video players, presenter programs) use different keyboard shortcuts, AndroHid provides a simple way for user defined keyboard mapping. This short HowTo contains all needed information to generate a user defined mapping.

### Keycodes and Modifiers ###

To map the different tab views of AndroHid, as eg. the player tab start the preferences menu and go to Settings --> Player tab mapping. You will find a list with entries called button 1 to 12. The entries correspond to the twelve buttons which you can see in the player tab view, where they are ordered in a 3 by 4 grid. The button numbering can be seen in the picture.

| ![https://androhid.googlecode.com/svn/images/view_button_indices.png](https://androhid.googlecode.com/svn/images/view_button_indices.png) |
|:------------------------------------------------------------------------------------------------------------------------------------------|
| Button numbering |

Clicking on one of the list entries you can adjust now two parameters called keycode and modifier. The keycode defines a keysignal as the user would produce one by hitting a key of his keyboard (eg. lower case letter "a" or number "2"). If the user wants to enter a capital letter "A" he simultaneously presses the "Shift" and "a" keys. The difference between lower case and upper case is represented by a varying modifier code. Examples for modifier keys are "Ctrl Right", "Ctrl Left" or "Alt". To combine several modifiers to a keystroke combination you have to add the modifier codes up ( to get "Right Alt" + "Right Ctrl" you obtain 1 + 4 = 5 for your modifier value).

### Examples ###

For better understanding have a look at some examples:

| Keystroke | Keycode | Modifier code |
|:----------|:--------|:--------------|
| "a" | 4 | 0 |
| "A" | 4 | 2 or 32 |
| "Ctrl" + "Alt" + "Delete" | 42 | 5 or 65 or 20 |
| "Left Gui" + "c" | 6 | 8 |
| "XF86AudioPlay" | 232 | 0 |

### Possible Keycodes and modifiers ###

Possible modifier codes are:

| Code | Modifier |
|:-----|:---------|
| 1 | Left Control |
| 2 | Left Shift |
| 4 | Left Alt |
| 8 | Left Gui |
| 16 | Right Control |
| 32 | Right Shift |
| 64 | Right Alt |
| 128 | Right Gui |

The following list of keycodes is not complete nor will it match different country keymappings. Eg. on a german keyboard the keycode 28 maps to "z" instead of "y" on US Keyboards. If you understood the logic guessing the right keycodes will be easy for you, just play around a bit...

| Keycode | Keyboard Signal |
|:--------|:----------------|
| 4 | a and A |
| 5 | b and B |
| 6 | c and C |
| 7 | d and D |
| 8 | e and E |
| 9 | f and F |
| 10 | g and G |
| 11 | h and H |
| 12 | i and I |
| 13 | j and J |
| 14 | k and K |
| 15 | l and L |
| 16 | m and M |
| 17 | n and N |
| 18 | o and O |
| 19 | p and P |
| 20 | q and Q |
| 21 | r and R |
| 22 | s and S |
| 23 | t and T |
| 24 | u and U |
| 25 | v and V |
| 26 | w and W |
| 27 | x and X |
| 28 | y and Y |
| 29 | z and Z |
| 30 | 1 |
| 31 | 2 |
| 32 | 3 |
| 33 | 4 |
| 34 | 5 |
| 35 | 6 |
| 36 | 7 |
| 37 | 8 |
| 38 | 9 |
| 39 | 0 |
| 40 | Return |
| 41 | Escape |
| 42 | Delete |
| 43 | Tab |
| 44 | Spacebar |
| 45 | - and |
| 46 | = and +  |
| 47 | [ and { |
| 48 | ] and } |
| 49 | \ and | |
| 50 | Non-US # and ~ |
| 51 | ; and : |
| 52 | ' and " |
| 53 | Tilde |
| 54 | , and < |
| 55 | . and > |
| 56 | / and ? |
| 57 | Caps Lock |
| 58 | F1 |
| 59 | F2 |
| 60 | F3 |
| 61 | F4 |
| 62 | F5 |
| 63 | F6 |
| 64 | F7 |
| 65 | F8 |
| 66 | F9 |
| 67 | F10 |
| 68 | F11 |
| 69 | F12 |
| 70 | Print Screen |
| 71 | Scroll Lock |
| 72 | Pause |
| 73 | Insert |
| 74 | Home |
| 75 | Page Up |
| 76 | Delete Forward |
| 77 | End |
| 78 | Page Down |
| 79 | Right Arrow |
| 80 | Left Arrow |
| 81 | Down Arrow |
| 82 | Up Arrow |
| 83 | Num Lock and Clear |
| 100 | Non-US \ and | |
| 101 | Application |
| 102 | Power |
| 103 | = |
| 104 | F13 |
| 105 | F14 |
| 106 | F15 |
| 107 | F16 |
| 108 | F17 |
| 109 | F18 |
| 110 | F19 |
| 111 | F20 |
| 112 | F21 |
| 113 | F22 |
| 114 | F23 |
| 115 | F24 |
| 116 | Execute |
| 117 | Help |
| 118 | Menu |
| 119 | Select |
| 120 | Stop |
| 121 | Again |
| 122 | Undo |
| 123 | Cut |
| 124 | Copy |
| 125 | Paste |
| 126 | Find |
| 127 | Mute |
| 128 | Volume Up |
| 129 | Volume Down |
| 130 | Locking Caps Lock |
| 131 | Locking Num Lock |
| 132 | Locking Scroll Lock |
| 224 | Left Control |
| 225 | Left Shift |
| 226 | Left Alt |
| 227 | Left GUI |
| 228 | Right Control |
| 229 | Right Shift |
| 230 | Right Alt |
| 231 | Right GUI |
| 232 | XF86AudioPlay |
| 233 | XF86AudioStop |
| 234 | XF86AudioPrev |
| 235 | XF86AudioNext |
| 236 | XF86Eject |
| 237 | XF86AudioRaiseVolume |
| 238 | XF86AudioLowerVolume |
| 239 | XF86AudioMute |
| 240 | XF86WWW |
| 241 | XF86Back |
| 242 | XF86Forward |
| 243 | Cancel |
| 244 | Find |
| 245 | XF86ScrollUp |
| 246 | XF86ScrollDown |
| 248 | XF86Sleep |
| 249 | XF86ScreenSaver |
| 250 | XF86Reload |
| 251 | XF86Calculator |