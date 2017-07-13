# Getting Started

Currently, we're promoting the [Gazelle System76 laptop](https://system76.com/laptops/gazelle) as a great starting laptop for new  developmers.  We recommend customizng the laptop to have Ubuntu 16.04 LTS installed.

## Ubuntu 16.04

(Run Terminal)[http://mixeduperic.com/linux/how-to-open-a-terminal-window-in-unity.html] then right click on it to (pin it)[https://i.stack.imgur.com/QaJaI.png] to your launcher.

While in Terminal, type these commands:

### Tools

```
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add - echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list sudo apt-get update
sudo apt-get update
sudo apt-get install git imagemagick sublime-text
touch ~/.bash_profile
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
source ~/.bashrc
nvm install 7.1.0
nvm use 7.1.0
npm install -g eslint htmllint-cli csslint
```

## Sublime

Now, run Sublime (Type `subl` in Terminal), pin it to your Launcher, and then follow the instructions here to install Package Control for Sublime: https://packagecontrol.io/installation (Copy the contents of the code in the Sublime Text 3 grey box on this website, then go to Sublime, press *ctrl + `* (That's not a _quote_, it's a _backtick_, to the left of the 1)to bring up the console window on the bottom, then paste the code into the bottom field of the console and press enter.))

Return to Sublime, press Shift + Control + P, a prompt will appear near the top center of the window, type `install package` and press enter.  When the prompt reappears, type an entry fro the list below and press enter.  Then repeat this process for every item in the list below:

```
SublimeLinter
SublimeLinter-contrib-eslint
SublimeLinter-csslint
SublimeLinter-contrib-htmllint
dockblockr
MarkdownLight
GitGutter
JSONLint
Typescript
PrettyJSON
SidebarEnhancements
EditorConfig
Color Highlighter
ColorPicker
```

### Github

