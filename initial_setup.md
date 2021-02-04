

# First things first, here's a guide to get you set up on installing Ubuntu to your Switch:

https://gbatemp.net/threads/l4t-ubuntu-a-fully-featured-linux-on-your-switch.537301/

## After you've got it set up, open a terminal (Ctrl + Alt + T or open `Terminal` from the app list), then copy and paste the following command to automatically update, then run the megascript: (hint: if running over ssh with no display, remove "gui")
>
    sudo apt update && sudo apt upgrade -y && sudo apt autoremove -y && sudo apt install bash gnutls-bin curl zenity -y && hash -r && bash <( curl https://raw.githubusercontent.com/cobalt2727/L4T-Megascript/master/core_refactor.sh ) "gui"

### IMPORTANT NOTE IF YOU GET ERRORS INVOLVING TURUL REPOSITORIES - run the following code to fix your update servers, then run the script again:
>
    sudo sed -E -i 's/turul.canonical/ports.ubuntu/g' /etc/apt/sources.list; sudo apt update

<br>
We HIGHLY recommend that you first run the initial setup script by entering `0` or `setup` to ensure everything is in working order. <br>
Here's all the options included in that:
<br>

## Swapfile
Needs 2 GB of space. Very important to avoid potential crashes and lag

## Joycon Mouse
Lets you use the joycons as - you guessed it - a mouse. <Br>
Default button configs: 
| Button | Key |
|------------- | ----- |
| B | Left Click |
| A | Right Click|
| X | Middle Mouse Button|
| L | Volume Down|
| R | Volume Up  |
|ZR| Brightness Up|
|ZL| Brightness Down|
|D-PAD| Keyboard Arrow Keys|
|Screenshot| Turn the mouse off and on (leave off when playing games)| 
|Home | Escape |
|+| Enter |
|-| Back |
## SDL2
Builds and installs SDL2. It's a _requirement_ for many games in the script, but can take some time to set up. <Br>
### The following programs require SDL2:
SRB2, SRB2Kart, CSE2-Tweaks, SuperTux2, TheXTech <br>
_List in progress_

## And that's all! You're all set to install any other program included in the megascript.  Check the individual wiki pages to read more on a particular game or program.
(You may want to hook up a USB keyboard and mouse to make setup easier...)
