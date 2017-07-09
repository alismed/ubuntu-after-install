## Ubuntu after install
My setup after install Ubuntu

**Update packages**

```
$ sudo apt-get upgrade
```

**Keyboard**

Execute the command below and follow the instructions
```
$ sudo dpkg-reconfigure keyboard-configuration
```

**System**

Hide user from login list

```
$ sudo apt-get install -y net-tools
$ sudo apt-get install -y htoop
$ sudo apt-get install -y glances
$ sudo apt-get install -y lib32-libstdc++5 glibc
$ sudo apt-get install -y ubuntu-make -y
```

**Text Editors**
```
$ sudo apt-get install -y vim

# Sublime Text
$ wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
$ echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
$ sudo apt-get update
$ sudo apt-get install sublime-text -y
```

**IDE's**
```
$ sudo apt-get install -y eclipse-jee
$ sudo apt-get install -y arduino
```

**Database**
```
$ sudo apt-get install -y mysql-clients
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
$ sudo apt-get install -y chromiun
$ sudo apt-get install -y firefox
$ sudo apt-get install -y flashplugin
$ sudo apt-get install -y wget curl
```

```
$ sudo apt-get install -y tar gzip bzip2 unzip unrar p7zip
```

**Languages**
```
$ sudo apt-get install -y openjdk-8-jdk
$ sudo apt-get install -y elixir

# Crystal
$ curl https://dist.crystal-lang.org/apt/setup.sh | sudo bash
$ apt-key adv --keyserver keys.gnupg.net --recv-keys 09617FD37CC06B54
$ echo "deb https://dist.crystal-lang.org/apt crystal main" > /etc/apt/sources.list.d/crystal.list
$ sudo apt-get update
$ sudo apt-get install crystal
$ sudo apt-get install build-essential
```

For Ruby, follow the instructions on [Ruby Verion Manager](https://rvm.io/rvm/install)

**Git**
```
$ sudo apt-get install -y git tig
```


**Docker**
```
$ sudo apt-get install -y docker
$ sudo gpasswd -a ${USER} docker
$ sudo systemctl enable docker
$ sudo systemctl start docker
```

**Nodejs**

Using [Node Version Manager](https://github.com/creationix/nvm)
```
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.1/install.sh | bash

# The script clones the nvm repository to ~/.nvm and adds the source line to your profile (~/.bash_profile, ~/.zshrc, ~/.profile, or ~/.bashrc).

# This loads nvm
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" 
```

**Install**

List the last version
```
$ nvm ls-remote
# choice the version
$ nvm install [x.x.x]
```

