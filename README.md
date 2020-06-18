# Development Machine Setup

## Table of Content

1. [Pre-requisites](#prerequisites)
2. [Homebrew Installation](#homebrew-installation)
3. [Languages, Editors, IDEs, & Useful Tools](#favorite-editor)

<a name="prerequisites"><a/>

## Prerequisites

The following instructions were executed on MacBook Pro running Catalina v10.15.4

1. XCode Command Line Tools

**Note** : If Xcode command line tools have not been installed, you will be prompted to accepts the terms and ```git``` will be installed

<a name="homebrew-installation"></a>

## Homebrew Installation

```
mkdir -p $HOME/Installations/Homebrew
cd $HOME/Installations/Homebrew
git clone https://github.com/Homebrew/brew.git
echo 'export PATH="$HOME/Installations/Homebrew/brew/bin:$PATH"' >> $HOME/.bash_profile
echo 'export PATH="$HOME/Installations/Homebrew/brew/Cellar/:$PATH"' >> $HOME/.bash_profile
echo 'export HOMEBREW_CASK_OPTS="--appdir=$HOME"/Installations/Homebrew/Applications --fontdir=$HOME/Homebrew/Library/Fonts"' >> $HOME/.bash_profile
source $HOME/.bash_profile
brew tap
brew tap homebrew/cask-versions
```

## Languages, Editors, IDEs, & Userful Tools


Node Version Manager
```
brew install nvm
mkdir $HOME/.nvm
echo 'export NVM_DIR="$HOME/.nvm"' >> $HOME/.bash_profile
echo '[ -s "$HOME/Installations/Homebrew/brew/opt/nvm/nvm.sh" ] \
 && . "$HOME/Installations/Homebrew/brew/opt/nvm/nvm.sh"' >> $HOME/.bash_profile
echo '[ -s "$HOME/Installations/Homebrew/brew/opt/nvm/etc/bash_completion.d/nvm" ] \
 && . "$HOME/Installations/Homebrew/brew/opt/nvm/etc/bash_completion.d/nvm"' >> $HOME/.bash_profile
source $HOME/.bash_profile
nvm -v
```

Node JS Installation
```
nvm install 12.16.3
nvm use --delete-prefix v12.16.3
node -v
npm -v
```

Java Version Manager & Java Installation

​		**Note**: adoptopenjdk8 Requires user password

```
brew install jenv
echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> $HOME/.bash_profile
echo 'eval "$(jenv init -)"' >> $HOME/.bash_profile
source $HOME/.bash_profile
brew cask install adoptopenjdk
brew cask install adoptopenjdk8
/usr/libexec/java_home -V 		# add the paths returned to jenv
jenv add /Library/Java/JavaVirtualMachines/adoptopenjdk-14.jdk/Contents/Home
jenv add /Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home
jenv enable-plugin maven
jenv enable-plugin export
jenv versions     						#To pick a specific version from the list
jenv global 1.8   						#1.8 is a value from the output of the above command, you may pick any other
```


Sublime Editor
```
brew cask install sublime-text2
```

Visual Studio Code
```
brew cask install visual-studio-code
```

IntelliJ IDEA
```
brew cask install intellij-idea
```

Postman
```
brew cask install postman
```

Typora
```
brew cask install typora
```

JQ 
``` 
brew install jq
```



