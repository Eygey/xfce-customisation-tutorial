this is a free github version of a xfce customisation tutorial for kali os
the end product will look something like this
![image](https://github.com/user-attachments/assets/c0a031c1-44e5-42e4-8525-34169accbeb9)


1. FILES
   download these files, two of them are in a google drive folder linked in the "fonrs and nordzy cyan dark mod" file.

2. INITIAL SETUP
   in your file manager press on "view" and show "hidden files"
   open terminal
   run: sudo apt update && sudo apt upgrade
   run: sudo apt install mugshot xfce4-terminal
     enter your password when needed
   (protip: add a -y at the end of your commands to confirm everything. If you don't you will have to press y at almost every command.)

3. ICONS, CURSORS AND FONTS
   hatsune miku cursor credit to supermariofps: https://github.com/supermariofps/hatsune-miku-windows-linux-cursors

  installing the theme:

   create a folder named .themes in your home folder. your home folder has the same name as your user.
    move the contents of GTK-XFWM-Theme.zip to ~/.themes


  installing the icon pack:

   create a folder named icons at ~/.local/share
   unzip Nordzy-cyan-dark-MOD.zip
  move the resulting Nordzy-cyan-dark-MOD folder to ~/.local/share/icons

  installing the cursor:

   unzip miku-cursor-linux.zip
   move the resulting folder miku-cursor-linux to /usr/share/icons/ (systemwide)
   right click on a empty space in that folder
   press "open as root"
   enter your password
   put the folder in there

installing the font:

   move the contents of fonts.zip to ~/.local/share/

4. INSTALLING KVANTUM
   run: sudo apt install qt5-style-kvantum qt5-style-kvantum-themes
   put the following kvantum folder into ~/.config

5. CHANGING THEME, ICONS, CURSORS, FONTS AND WALLPAPER
   open settings manager

    applying theme

   open appearance settings
    select the style tab appearance settings
    select Everblush_GTK_THEME

    applying the icons 
     select the Icons tab in appearance settings
     select Nordzy-cyan-dark-mod
   
    applying fonts
     select the fonts tab appearance settings
     select roboto regular as your default font
     select Jetbrains nerd mono regular

    applying the cursor

     open settings, select mouse and touchpad
     select themes
     select the miku cursor
   
    applying the new wallpaper

     search for your preferred background, doesn't matter what, but preferably a dark one
     download it
     go into settings, select desktop
     in the bottom left corner of the window press on folder
     select your downloads folder
     select your preferred image

   6. CONFIGURING LIGHTDM LOGIN MANAGER
      open terminal
      run: cd .themes   
      run: sudo cp -R Everblush /usr/share/themes/
      enter your password if needed
      run: cd
      run: cd .local
      run: cd share
      run: cd icons
      run: sudo cp -Rv Nordzy-cyan-dark-MOD /usr/share/icons
        enter your password if needed (mild epillepsy warning)
      open lightdm GTK+ greeter settings
      enter your password
      change your theme to everblush
      change your icons to Nordzy-cyan-dark-MOD
      change the image to your previously chosen wallpaper
      change your user image if you want

   7. CONFIGURE XFCE4 PANEL
      open terminal
      run: xfce4-panel --quit (your taskbar will be gone don't be shocked)
      run: pkill xfconfd
      open file manager (press the windows key on your keyboard)
      unzip home-config.zip
      move its contents into your home folder
      in the same folder find the ".profile" file and rename it ".profile-00" as to not conflict with our profile file
      move the ".profile" and ".Xresources" file from the home-config folder to your home folder
      unzip gtk-3.0-css.zip
      go to ~/config/gtk-3.0
      move "gtk.css" from the gth-3.0-css folder to ~/config/gtk-3.0
      unzip xfce4-config
      go to your .config folder
      rename the xfce4 folder to "xfce-00"
      move xfce4 from xfce4-config to your .config folder
      go to the xfce4 folder
      if you have changed the default user name of the user then you must go to ~/.config/xfce4/panel
      open the genmon15.rc, genmon16.rc and genmon17.rc and in the first line change kali to the username
      do the same to whiskermenu-8.rc on the fourth line
      run: xfce4-panel &
      you can customise the panel by opening the panel application
