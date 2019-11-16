# Fix color emoji in Chrome and Firefox

## Why?

Chrome and Firefox don't seem to support colored emoji out of the box on elementaryOS. This fixes that issue.

## How?

Make a new empty file called `01-emoji.conf` in `~/.config/fontconfig/conf.d/`. If the path doesn't exist, just create it manually. Open the empty file in your preferred text editor and put the content below.

	<?xml version="1.0" encoding="UTF-8"?>
	<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
	<fontconfig>
	<alias>
		<family>serif</family>
		<prefer>
		<family>Noto Color Emoji</family>
		</prefer>
	</alias>
	<alias>
		<family>sans-serif</family>
		<prefer>
		<family>Noto Color Emoji</family>
		</prefer>
	</alias>
	<alias>
		<family>monospace</family>
		<prefer>
		<family>Noto Color Emoji</family>
		</prefer>
	</alias>
	</fontconfig>

Afterwards, clear the font cache by running the following command in Terminal.

	`fc-cache -f -v`

Then just re-open the application(s). You can also restart if you want.

---
[elementary-patches](https://github.com/sprite-1/elementary-patches)