Update for avoiding bell sound when VIM is in command mode

User Allen Castaban pointed out that VIM will sometimes generate an annoying bell sound when using this extension.  To be exact, the bell sound will be generated if VIM is already in command mode when this extension is used.  Allen further suggested a way that can avoid this bell sound(issue INSERT first and then issue ESC).  This has been coded and proved to work well.  The only side effect is that cursor is moved left by one character in some instances.

The only updated source file is gvimext.cpp.

June 13, 2007

Notes for opening files under tabs in VIM using the gvimext.dll right-click context menu:
-.  UseTab.reg
This file will add the following registry value:
[HKEY_LOCAL_MACHINE\SOFTWARE\Vim\Gvim]
"UseTab"="1"
The above value will make the "Edit with ... using tabs" context menu as the defaul menu.
To import this reg file, right-click it and choose Merge in Windows Explorer.
-.  Shift key effect
Shift key serves as a toggle key for the "Edit with ... using tabs" context menu.  If you hold down the Shift key and then right-click the selectec files in Windows Explorer, the opposite of the default Vim context menu will display.
Once the Vim content menu displays, you don't need to hold down the Shift key anymore.  Its effect will hold even until the next Right-Click.

Tianmiao Hu
September 19, 2006
