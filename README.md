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

# ssh key
$ ssh-keygen -t rsa -b 4096 -C "<your_email@example.com>"
cat ~/.ssh/id_rsa.pub
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
# Mame
$ sudo apt-get install -y mame 
$ mkdir -p ~/mame/roms

# DosBox
$ sudo snap install dosbox-x
```

**Databases Clients**
```
$ sudo apt-get install -y mysql-client
$ sudo apt-get install -y postgresql-client
$ sudo apt-get install -y redis-tools

**MongoDB v4.0**
$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4
$ echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list
$ sudo apt-get install pmongodb-org-tools mongodb-org-shell -y
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

**Elixir**
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

**Python 3**
```
$ sudo apt-get install -y python3-pip
$ sudo apt-get install -y python3-venv
```

For Ruby, follow the instructions on [Ruby Verion Manager](https://rvm.io/rvm/install)

**.Net Core**
```
$ wget -q https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb
$ sudo dpkg -i packages-microsoft-prod.deb
$ sudo apt-get install apt-transport-https
$ sudo apt-get update
$ sudo apt-get install -y dotnet-hosting-2.0.8

#.NET SDK
$ sudo add-apt-repository universe
$ sudo apt-get install apt-transport-https
$ sudo apt-get update
$ sudo apt-get install dotnet-sdk-2.2
```

**Kotlin**
```
# first install java 8 or later

$ sudo snap install kotlin --classic
```

**GO Lang**
```
sudo snap install --classic go
export GOPATH=$HOME/go
```

**Heroku Cli**
```
# first install java 8 or later
$ sudo snap install heroku --classic
```

**Salesforce Cli**
```
$ wget https://developer.salesforce.com/media/salesforce-cli/sfdx-linux-amd64.tar.xz
$ mkdir sfdx
$ tar xJf sfdx-linux-amd64.tar.xz -C sfdx --strip-components 1
$ ./sfdx/install
```

**Text Editors**
```
$ sudo apt-get install -y vim
```
For Vundle, [follow this](https://github.com/alismed/vimfiles).


**Postman**
```
$ sudo snap install postman
```

**Sublime Text**
```
$ wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
$ echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
$ sudo apt-get update
$ sudo apt-get install sublime-text -y
```

**Visual Studio Code**
```
$ sudo snap install vscode --classic
```

**IDE's**
```
$ sudo apt-get install fritzing
$ sudo snap install eclipse --clasic
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

**Social**
```
$ sudo snap spotify
```

**Video**
```
$ sudo snap vlc
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

# Docker Compose
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
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

_Install_

List the versions
```
$ nvm ls-remote
# choice the version
$ nvm install [x.x.x]
```

[Install packages](https://github.com/alismed/npm-package-install)


**Yarn**
```
$ sudo apt-get install -y --no-install-recommends yarn
```

**Communicators**
```
$ sudo apt-get install -y --no-install-recommends yarn
# is necessary restart after install
$ sudo snap install slack --classic
$ sudo snap install skype --classic
```

