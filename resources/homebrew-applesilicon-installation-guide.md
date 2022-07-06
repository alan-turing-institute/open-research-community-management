# Apple M1 Homebrew Installaton 

There are documented issues with installing Homebrew (a popular package manager used by data scientists, developers, and research software engineers) on new Apple computers that come with the Apple Silicon (M1 or M2) chips. 

Side Note: If you don't have your Mac set up with a password (including if the password is blank) you will not be able to install Homebrew.

To instally Homebrew on machines running in Apple Silicon, run through the following steps:

### 0. Check Installs Run the usual checks on if homebrew is installed:

`% brew`

If it is then that's okay, but you want to be checking the $PATH prefix to see if it's `/usr/local/bin` (the standard place Homebrew installs which works for Intel chips) **or** if `/opt/homebrew` is on your $PATH which makes Homebrew Apple Silicon friendly. 

So to debug:

### 1. Install Homebrew
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

On Apple Silicon machines the Homebrew files are installed into the `/opt/homebrew` folder. But the folder is not part of the default `$PATH` so we need to create a `~/.zprofile` file which contains a command which sets up Homebrew.

### 2. Create a `~/.zprofile` file
Run the following two commands: in your terminal
`echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/sbatchelor/.zprofile`
`eval "$(/opt/homebrew/bin/brew shellenv)"`

### 3. Check the install 

Run `brew doctor` which should return `Your system is ready to brew` if things worked properly. 

On Apple Silicon, if you see `zsh: command not found: brew`, check that you've created a ~/.zprofile file as described above and restart terminal.

If Homebrew is successfully installed, there will be Homebrew files in `/opt/homebrew` and you'll get the `Your system is ready to brew` message after running `brew doctor`. 

--- 

### Alternative routes:

If the above didn't work then the stackoverflow consensus is that the following commands will work (but I haven't tried them myself): 

`git clone https://github.com/Homebrew/brew homebrew`
`eval "$(homebrew/bin/brew shellenv)"`
`brew update --force --quiet`
`chmod -R go-w "$(brew --prefix)/share/zsh"`
