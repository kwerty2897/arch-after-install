###SRACH AFTER INSTALL###


##disable beeper##
$ sudo echo "blacklist pcspkr" | sudo tee -a /etc/modprobe.d/blacklist-pcspkr.conf  

##отсортирует зеркала по скорости и обновит mirrorlist##
$ sudo pacman -Sy reflector rsync
$ sudo reflector -c 'Russia' -f 12 -l 12 -n 12 --verbose --save /etc/pacman.d/mirrorlist 

##nvidia driver (maxwell and newer)##
$ sudo pacman -S nvidia

##ntp setup##
$ sudo systemctl enable systemd-timesyncd 
$ sudo systemctl start systemd-timesyncd 

$ sudo nano /etc/systemd/timesyncd.conf

[Time]
NTP=0.arch.pool.ntp.org 1.arch.pool.ntp.org 2.arch.pool.ntp.org 3.arch.pool.ntp.org
FallbackNTP=0.pool.ntp.org 1.pool.ntp.org 0.fr.pool.ntp.org

$ sudo timedatectl set-ntp true

##фиксим мыльные шрифты в gtk4##
$ nano ~/.config/gtk-4.0/settings.ini

gtk-hint-font-metrics=true





###CTLOS AFTER INSTALL###


##from sddm to lightdm##
$ sudo pacman -S lightdm lightdm-gtk-greeter lightdm-gtk-greeter-settings 
$ sudo systemctl disable sddm
$ sudo systemctl enable lightdm 
$ sudo pacman -Rsc sddm
