# st - simple terminal


st is a simple terminal emulator for X which sucks less.

## TODO
{}properly add boxdraw

## Requirements

In order to build st you need the Xlib header files.
The font used is JetBrainsMono as a patched NerdFont.
Install on Arch:

    pacman -S nerd-fonts-jetbrains-mono ttf-joypixels

## Installation


Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

## Patches


### anygeometry

Lets st be any geometry to work with gaps in tiling window managers.

### blinking cursor

Gives the possibility of a blinking cursor.
The cursor is set not to blink.
Can be changed in the config.def.h at `cursorshape`.

### bold is not bright

Renders bold text as actual bold and not bright text.

### boxdraw

Enables smooth drawing of lines. Nice to have for tmux.

### clipboard

Makes the st clipboard the same as system one.

### delkey

Makes the delkey behave properly.

### desktopentry

Adds a desktopentry for st, so it can be found by launchers.

### focus and alpha

Adds alpha values so st can be transparent. Focus adds different values depending on if the terminal is focused or not.

### font2

Adds a second font to support symbols that are not present in the first font.

### ligatures

Adds ligature support.

### newterm

Adds the amazing shortcut `ctr+shift+return` to open another terminal in the same cwd.

### rightclickpaste

Adds the ability to use the right mouse button to paste the clipboard.

### swapmouse

Uses the proper cursor in applications like ranger.

### themed cursor

Uses the cursor that is defined in the x-theme.

### Scrollback

Adds a scrollback buffer.

## Running st


If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Credits


Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
