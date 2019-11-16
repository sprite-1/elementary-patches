# Decrease the gap between system tray icons

## Why?

By default system tray icons in elementaryOS have some gap to let them breathe with spacing. However some people want more compact icons packed closer to each other.

## How?

Open `/usr/share/themes/elementary/gtk-3.0/apps.css` and find the `.composited-indicator` line. Set its `padding` value to `0px` and restart.

	.composited-indicator {
		padding: 0px;
	}

> __NEWBIE TIP:__ You need root permission to edit this file. So open up the Terminal and paste the following:  
`sudo io.elementary.code /usr/share/themes/elementary/gtk-3.0/apps.css`  
Enter your user password once you're asked for it. This will open an elevated instance of Code so you can make your changes properly.

If everything went accordingly, you should see the difference.

__Before__

![screenshot1](screenshot1.png)

__After__

![screenshot2](screenshot2.png)