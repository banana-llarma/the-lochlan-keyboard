## this is malachi's notes on qmk using the kbd67

- you will need git and qmk to be installed
- to install qmk properly go to `https://docs.qmk.fm/#/newbs_getting_started`
- if a line starts with a $ then it means it is a terminal command

### make a keymap

- clone the git repo  
$ `git clone git@github.com:banana-llarma/the-lochlan-keyboard.git ~/the-lochlan-keyboard`

- link the template  
$ `mkdir ~/qmk_firmware/keyboards/kbdfans/kbd67/rev2/keymaps/the-lochlan-keyboard && ln -f ~/the-lochlan-keyboard ~/qmk_firmware/keyboards/kbdfans/kbd67/rev2/keymaps/the-lochlan-keyboard`

- now you can change your keyboard layout in the `keymap.c` file in `~/the-lochlan-keyboard/template` directory
- to flash the new keyboard settings run  
$ `qmk flash -kb kbdfans/kbd67/rev2 -km the-lochlan-keyboard`
- if that doesn't work make sure you are in `~/qmk_firmware` directory

- run this if the command about doesn't work
$ `cd ~/qmk_firmware && sudo qmk flash -kb kbdfans/kbd67/rev2 -km the-lochlan-keyboard`
