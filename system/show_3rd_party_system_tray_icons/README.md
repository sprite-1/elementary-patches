# Show 3rd party system tray icons

## Why?

Some applications rely on the use of system tray icons for its usability. Unfortunately, elementaryOS has already deprecated this feature. You can still restore this, however.

## How?

1. Make `indicator-application` recognize Pantheon. Open Terminal and run the following commands.  
`mkdir -p ~/.config/autostart`  
`cp /etc/xdg/autostart/indicator-application.desktop ~/.config/autostart/`  
`sed -i 's/^OnlyShowIn.*/OnlyShowIn=Unity;GNOME;Pantheon;/' ~/.config/autostart/indicator-application.desktop`
2. Download latest available release of wingpanel-indicator-ayatana.  
`wget http://ppa.launchpad.net/elementary-os/stable/ubuntu/pool/main/w/wingpanel-indicator-ayatana/wingpanel-indicator-ayatana_2.0.3+r27+pkg17~ubuntu0.4.1.1_amd64.deb`
3. Install it.  
`sudo dpkg -i wingpanel-indicator-ayatana_2.0.3+r27+pkg17~ubuntu0.4.1.1_amd64.deb`

> __CAVEAT:__ While this shows the 3rd party system tray icons again, because of the way elementaryOS has been themed, there will be huge gaps between them. To fix this, please read ["Decrease the gap between system tray icons"](https://github.com/sprite-1/elementary-patches/tree/master/design/decrease_the_gap_between_system_tray_icons).

![screenshot1](screenshot1.png)

---
[elementary-patches](https://github.com/sprite-1/elementary-patches)