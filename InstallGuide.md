## Git
1. Install
  * Windows
    * Git for Windows (https://git-for-windows.github.io/)
    * Use Git Bash as your terminal from now on.
      * Tips for Git Bash
        * Copy is ctrl + insert
        * Paste is shift + insert
  * Mac
    * Download and install from http://git-scm.com/downloads
    * Highly recommend using [iTerm2](https://www.iterm2.com/) as your terminal
1. Restart your terminal
1. Type `git --version`, you should see a version number.

## Sublime Text 3
1. You do not have to use this text editor, but it is industry level with a great [plugin community](https://packagecontrol.io/).
1. Download and install from http://www.sublimetext.com/3
1. Add Sublime Text shortcut
  * (Mac) run `echo "alias subl='/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl'" >> ~/.bash_profile`
  * (Windows) run  `echo "alias subl='/c/Program\ Files/Sublime\ Text\ 3/subl'" >> ~/.bash_profile`
1. Restart your terminal.
1. You should be able to access Sublime Text from the command line by typing `subl`.
  * If not, we will troubleshoot the first day of class.

## Node.js
1. Download and install from https://nodejs.org/
1. Restart terminal
1. type `node -v`, should get a version number if it works.

## Google Chrome Browser
* Download and install from http://www.google.com/chrome/

## Postman App (Chrome Browser)
* Download and install from [here](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=en)

## MAMP
1. Download and install from https://www.mamp.info/en/
  * You do not need to install MAMP Pro
1. Find highest `php` version
  * (Mac) In your terminal, run `ls /Applications/MAMP/bin/php/` for your list of available versions
  * (Windows) In your terminal, run `ls /c/MAMP/bin/php/` for your list of available versions
1. Add MAMP php to path
  * (Mac) run using the selected version `echo 'export PATH=/Applications/MAMP/bin/php/php5.6.10/bin:$PATH' >> ~/.bash_profile`
  * (Windows)
    1. Run using the selected version `echo 'export PATH=/c/MAMP/bin/php/php5.6.10/:$PATH' >> ~/.bash_profile`
    1. Go to your Control Panel > System and Security > System > Advanced System Settings > Environment Variables
    1. Add a new "System Variable" `PHPRC` with a value of `C:\MAMP\conf\php5.6.10` (using your version number). Click OK, Ok and exit.
1. Restart terminal
1. Type `which php` in terminal, should see `MAMP` in the file path

## SQLite Browser
* Download and install from http://sqlitebrowser.org/

## Heroku Toolbelt
* Download and install from https://toolbelt.heroku.com/

## Composer
1. In your terminal, navigate into your home directory `cd`
1. Download and install composer
  * Mac
    1. Run `sudo mkdir -p /usr/local/bin`
    1. Run `curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer`
    2. Run `echo 'export PATH=~/.composer/vendor/bin:$PATH' >> ~/.bash_profile`
  * Windows
    1. Download and install from https://getcomposer.org/Composer-Setup.exe
    1. When prompted for your PHP path, enter `C:\MAMP\bin\php\php5.6.10\php.exe` using your selected version from earlier
    1. Run `echo 'export PATH=/c/Users/<username>/AppData/Roaming/Composer/vendor/bin:$PATH' >> ~/.bash_profile`, replacing `<username>` with your username (the name of your user folder)

1. restart terminal

## Laravel Package
* run `composer global require "laravel/installer"`
