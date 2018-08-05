## Ubuntu after install
My setup after install Ubuntu 18.04.1

**Update packages**

```
$ sudo apt-get upgrade
```

**Keyboard**

Execute the command below and follow the instructions
```
$ sudo dpkg-reconfigure keyboard-configuration
```

**Login**

Hide user from login list

Create the file /etc/dconf/profile/gdm
```
user-db:user
system-db:gdm
file-db:/usr/share/gdm/greeter.dconf-defaults
```

Create the directory:
```
sudo mkdir /etc/dconf/db/gdm.d
```

Create the file /etc/dconf/db/gdm.d/00-login-screen:
```
[org/gnome/login-screen]
# Do not show the user list
disable-user-list=true
```

Execute
```
$ sudo dconf update
```

**Git**
```
$ sudo apt-get install -y git tig
```

**System**

```
$ sudo apt-get install -y snap
$ sudo apt-get install -y cowsay fortune
$ sudo apt-get install -y net-tools
$ sudo apt-get install -y htop
$ sudo apt-get install -y glances
$ sudo apt-get install -y putty
$ sudo apt-get install -y gnupg2
$ sudo apt-get install -y ubuntu-make
```

**Games**
```
$ sudo apt-get install -y zsnes
$ sudo apt-get install -y stella
$ sudo apt-get install -y mame mame-extra
```

**Database**
```
$ sudo apt-get install -y mysql-client
$ sudo apt-get install -y postgresql-client
$ sudo apt-get install -y redis-tools
```

**Languages**
```
$ sudo apt-get install -y openjdk-8-jdk

# Java Home
$ vim ~/.profile
  JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64

$ source ~/.profile

# Maven
$ sudo apt-get install -y maven
```

## Elixir
```
$ sudo apt-get install -y elixir

## Crystal
$ curl https://dist.crystal-lang.org/apt/setup.sh | sudo bash
$ apt-key adv --keyserver keys.gnupg.net --recv-keys 09617FD37CC06B54
$ echo "deb https://dist.crystal-lang.org/apt crystal main" > sudo /etc/apt/sources.list.d/crystal.list
$ sudo apt-get update
$ sudo apt-get install crystal
$ sudo apt-get install build-essential
```

## Python 3
```
$ sudo apt-get install -y python3-pip
$ sudo apt-get install -y python3-venv
```

For Ruby, follow the instructions on [Ruby Verion Manager](https://rvm.io/rvm/install)

## .Net Core
```
$ wget -q https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb
$ sudo dpkg -i packages-microsoft-prod.deb
$ sudo apt-get install apt-transport-https
$ sudo apt-get update
$ sudo apt-get install -y dotnet-hosting-2.0.8
```

## Kotlin
```
# first install java 8 or later
$ wget -O sdk.install.sh "https://get.sdkman.io"
$ bash sdk.install.sh
$ source ~/.sdkman/bin/sdkman-init.sh 
$ sdk install kotlin
```

**Text Editors**
```
$ sudo apt-get install -y vim
```
For Vundle, [follow this](https://github.com/alismed/vimfiles).


**Postman**
```
snap install postman
```

**Sublime Text**
```
$ wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
$ echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
$ sudo apt-get update
$ sudo apt-get install sublime-text -y
```

**Visual Studio Code**

Download the .deb from [ofcial web site](https://code.visualstudio.com/) and execute the package.

**IDE's**
```
$ sudo apt-get install fritzing
$ umake ide eclipse-jee
$ umake ide eclipse-php
$ umake ide eclipse-cpp
$ sudo apt-get install -y arduino

```

**Android Studio**

[Download](https://developer.android.com/studio/) the lastest version.
```
# requisites
$ sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386
- Unzip the package in /usr/local/
- Run the /usr/local/android-studio/bin/studio.sh and follow the instructions
- Will take a few minutes to finish
```

**Terminal**
```
$ sudo apt-get install -y terminator
$ sudo apt-get install -y zsh
$ sudo apt-get install -y tmux
```
Oh my ZSH
```
$ sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

**Fonts**
```
$ sudo apt-get install -y ttf-dejavu

# Power Line
$ git clone https://github.com/powerline/fonts.git
$ cd fonts
$ ./install.sh
$ cd ..
$ rm -rf fonts
```

**Image Editor**
```
$ sudo apt-get install -y gimp
$ sudo apt-get install -y imagemagick
```

**Browsers**
```
$ sudo apt-get install -y chromium-browser
$ sudo apt-get install -y lynx
$ sudo apt-get install -y wget curl
```

**Docker**
```
$ sudo apt-get install apt-transport-https ca-certificates software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
$ sudo apt-get update
$ sudo apt-get install -y docker-ce
$ sudo gpasswd -a ${USER} docker
$ sudo systemctl enable docker
$ sudo systemctl start docker
```

**Nodejs**

Using [Node Version Manager](https://github.com/creationix/nvm)
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash

# The script clones the nvm repository to ~/.nvm and adds the source line 
# to your profile (~/.bash_profile, ~/.zshrc, ~/.profile, or ~/.bashrc).

# This loads nvm
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" 

# execute
$ source ~/<profile-file>
```

**Install**

List the last version
```
$ nvm ls-remote
# choice the version
$ nvm install [x.x.x]
```

[Install packages](https://github.com/alismed/npm-package-install)


**Communicators**
```
# is necessary restart after install
$ sudo snap install slack --classic
$ sudo snap install skype --classic

