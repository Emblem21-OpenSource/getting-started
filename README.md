# Getting Started

Currently, we're promoting the [Gazelle System76 laptop](https://system76.com/laptops/gazelle) as a great starting laptop for new  developmers.  We recommend customizng the laptop to have Ubuntu 16.04 LTS installed.

## Ubuntu 16.04

(Run Terminal)[http://mixeduperic.com/linux/how-to-open-a-terminal-window-in-unity.html] then right click on it to (pin it)[https://i.stack.imgur.com/QaJaI.png] to your launcher.

While in Terminal, type these commands:

### Tools

```
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
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

Next, create an email address just for you that will deal with your life as a programmer.  Then, create an account at http://www.github.com

Now return to Terminal and type whoami and that will give you your Username.  You'll need this later.

Next, you'll have to generate an SSH key with this:

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Replace `your_email@example.com` with the email address you've created

Once here, you'll go through a prompt that will ask `Enter a file in which to save the key (/home/<whateverYourUsernameIs>/.ssh/id_rsa):`

Type (Don't paste, you CANNOT paste here) `/home/<whoeverYourUserNameIs>/.ssh/github_rsa` and press enter.

It will ask you for passwords, enter something easy to remember.

Then when this is done, type `chmod 0600 ~/.ssh/github_rsa`

Then type `gedit ~/.ssh/config`  This will open gedit and paste the following into it

```
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/github_rsa
```

When you are done, press `ctl + s` to save the file, then close gedit.

NOW, return to Terminal and type `cat ~/.ssh/github_rsa.pub`  This will output the file contents on the terminal.  Select those contents and copy them then go to https://github.com/settings/keys (Make sure you are logged in) and click on the green button called New SSH Key in the upper right hand corner.

Set the Title field to `System76 Laptop` and then paste your clipboard contents to the Key field and click on the green `Add SSH Key` button below.

Then go back to Terminal and type `ssh git@github.com` and type `yes`, press enter, and when it asks you for a password, enter it, and press enter.

Gradulations, you are now ready to be a Web Developer for Emblem 21!

## Windows

Open Git Bash

Next, you'll have to generate an SSH key with this:

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Replace `your_email@example.com` with the email address you've used for GitHub

Once here, you'll go through a prompt that will ask `Enter a file in which to save the key:`  Just press enter.

It will ask you for a password, enter something easy to remember. Press enter, then type:

```
git config --global user.name "your github name"
git config --global user.email "your github email"
mv ~/.ssh/id_rsa ~/.ssh/github_rsa
mv ~/.ssh/id_rsa.pub ~/.ssh/github_rsa.pub
chmod 0600 ~/.ssh/github_rsa
```

Then type `notepad ~/.ssh/config`  This will open notepad and paste the following into it:

```
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/github_rsa
```

When you are done, press `ctl + s` to save the file, then close notepad.

NOW, return to Git Bash and type `cat ~/.ssh/github_rsa.pub`  This will output the file contents on the terminal.  Select those contents and copy them then go to https://github.com/settings/keys (Make sure you are logged in) and click on the green button called New SSH Key in the upper right hand corner.

Set the Title field to `My Trusty Desktop` and then paste your clipboard contents to the Key field and click on the green `Add SSH Key` button below.

Then go back to Terminal and type `ssh git@github.com` and type `yes`, press enter, and when it asks you for a password, enter it, and press enter.
