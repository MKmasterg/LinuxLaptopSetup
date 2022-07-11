# LinuxLaptopSetup

A personal guide to setting up an efficient GNU/Linux for laptops!

  

The distro itself doesn't matter honestly (except the how-to s or the functiality) but I mainly use Fedora just so you know :)

# GUI Look&Feel
Basic Intro:
 - Desktop Environment (like [Gnome](https://www.gnome.org/) or [KDE](https://kde.org/)) : Most distros including fedora use DE, because they are more user-friendly and they come with a lot of utilities (like audio configs) that a mere Window Manager doesn't have.
 - Window Manager (like [awesome](awesomewm.org) or [i3](i3wm.org)): They don't have utilities like DEs and they are NOT user-friendly :| but when you learn how to work with them, you're gonna love WM. because you can navigate through windows and workspaces without using mouse (or less using mouse), like who doesn't want that?!
 I personally use both of them.  
 
 **Desktop Environment** 
 I primary use Gnome, and I have just a theme as Gnome configs!
 for installing Gnome and login [flat-remix-themes](https://drasite.com/flat-remix-gnome):
` sudo dnf copr enable daniruiz/flat-remix`
`sudo dnf install flat-remix-gnome`

**Window Manager**
I personally use and like [awesome wm](https://awesomewm.org/) , but to be honest [i3](i3wm.org)'s hotkeys make more sense than awesome's. but don't worry you can always change the default hotkeys!

Typically window managers are tricky and I still can't figure out most of the things! but at least I'm satisfied at the look and feel of awesome wm that I configured.

**Theme**
I actually don't care about theming, but yeah even I need a comfy workspace to work with!
So I chose the [copy-cats themes](https://github.com/lcpz/awesome-copycats), they are beautiful and easy to work with. I chose Black Burn for now. You can follow the instructions in the repo but I've already put my configs (that comes from the copy-cats themes rc.lua template) in my repository, but make sure you install the dependencies.  

**Configs**
The configs are not a big deal, everything is in the `rc.lua` (better put your settings in your home directory at `.configs/`, if not exist you can usually find the templates at 

    /etc/xdg/
    #or 
    /usr/share 
   make a copy of them and put them in your home directory.)
**Installation Guide**

 1. Install awesome using `sudo dnf install awesome`.
 2. Put the `rc.lua`& `themes/` into your home directory : `~/.config/awesome/` 
 3. Now install the [dependencies](https://github.com/lcpz/awesome-copycats#notes) that copy-cats theme needs.
 4. Install [Compton](https://github.com/chjj/compton) using `sudo dnf install compton` and put the `compton.conf` into your home directory : `~/.config/compton/compton.conf`
 5. Install Rofi, for the dmenu (or run prompt to be specific) I used Rofi, make sure you install Rofi and also Its theme: `sudo svn checkout https://github.com/lr-tech/rofi-themes-collection/trunk/themes` put them in `~/.local/share/rofi/themes`
 6. Last but not least install awesome fonts, for font based icons : `sudo dnf install fontawesome-fonts`

**Terminal shell**
Have you ever wondered why your terminal look and feel seems lame? then I think you should consider using [zsh](https://www.zsh.org/)!
Your default terminal shell is probably bash, so we want to change this to zsh, because we want plugins and the customizations!
**Installing & configuring zsh**
Install the zsh itself by using `sudo dnf install zsh`. there is this thing called [oh-my-zsh](https://ohmyz.sh/) that made our works much easier for configurations and customizations! 
Use wget for downloading the framework: 
`wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh`
then run it : `sudo bash ./install.sh`
Now we want to add our plugins and themes.