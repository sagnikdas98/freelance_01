# freelance_01
INSTRUCTIONS: splash screen
1.Open terminal and run: gksudo pcmanfm
2.Rename your desired picture as "splash.jpg" and copy it to "/etc" folder
3.Paste file "asplashscreen.service" in "/etc/systemd/system"
4.Open a new terminal and run: sudo nano /boot/config.txt
5.Paste the contents of "config.txt" at the end of the file
6.Run: sudo nano /boot/cmdline.txt
7.Paste the contents of "cmdline.txt" at the end of the line
Run: sudo apt install fbi
Run: sudo systemctl enable asplashscreen
Run: sudo systemctl start asplashscreen
Run: sudo reboot


________________________________
For video splash screen:
1.Run: sudo apt install omxplayer
2.Rename youe video as "splashv.mp4" and copy it to "/etc" folder
3.Replace line 7 of file "asplashscreen.service" with "ExecStart=/usr/bin/omxplayer -b /etc/splashv.mp4"
Run: sudo systemctl enable asplashscreen
Run: sudo systemctl start asplashscreen
________________________________
CEC commands:

1.Run: sudo apt-get install cec-utils

TV off command: echo "standby 0" | cec-client RPI -s -d 1
TV on command: echo "on 0" | cec-client RPI -s -d 1
