i3lock-fancy
============

i3lock script that takes a screenshot of the desktop, blurs the background and adds a lock icon and text

Depends:
* [i3lock-color-git](https://github.com/eBrnd/i3lock-color)
* imagemagick
* scrot
* Liberation Fonts

Screenshot:

![lockscreen](https://raw.githubusercontent.com/meskarune/i3lock-fancy/master/screenshot.png)

Use this with xautolock to automatically lock the screen after a set time.

Systemd Unit file (edit for your own use):

    [Unit]
    Description=Lock the screen automatically after a timeout
    
    [Service]
    Type=simple
    User=meskarune
    Environment=DISPLAY=:0
    ExecStart=/usr/bin/xautolock -time 5 -locker /usr/local/bin/lock/lock -detectsleep
    
    [Install]
    WantedBy=graphical.target
