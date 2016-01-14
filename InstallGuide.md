## Git
* Install
  * Windows
    * Git for Windows (https://git-for-windows.github.io/)
    * Use this terminal from now on.
  * Mac OS X and Linux
    * Download and install from http://git-scm.com/downloads
* Test if it works
  * Restart your terminal and type `git --version`, should get a version number if it works.

## Sublime Text 3
* You do not have to use this text editor, but it is industry level with a great [plugin community](https://packagecontrol.io/).
* Download it from http://www.sublimetext.com/3
* (Mac) Try running `echo "alias subl='/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl'" >> ~/.bash_profile` then restart your terminal.
  * If successful, you will be able to access Sublime Text from the commmand line by typing `subl` . If not, we will troubleshoot the first day of class.
* (Windows) `subl.exe` in your command line may already work. If not, try and follow the instructions [here](https://scotch.io/tutorials/open-sublime-text-from-the-command-line-using-subl-exe-windows).

## Node.js
* Download and install from https://nodejs.org/
* Restart terminal, type `node -v`, should get a version number if it works.

## Google Chrome Browser
* Download and install from http://www.google.com/chrome/

## Postman App (Chrome Browser)
* Download and install from https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=en

## MAMP
* Download from https://www.mamp.info/en/
* Mac/Linux
  1. run `echo "export PATH=/Applications/MAMP/bin/php/php5.6.10/bin:$PATH" >> ~/.bash_profile` then restart your terminal.
  1. then try `which php` and check to see if `MAMP` is in the file path.
* Windows
  1. Stay tuned

## SQLite Browser
* Download and install from http://sqlitebrowser.org/

## Heroku Toolbelt
* Download and install from https://toolbelt.heroku.com/

## Composer
* Run `curl -sS https://getcomposer.org/installer | php` in your terminal
  * Mac/Linux
    1. Run `echo "export PATH=~/.composer/vendor/bin:$PATH" >> ~/.bash_profile`
    1. You need to move your `composer.phar` into your path. In the terminal (navigated inside the directory with `composer.phar`) run `mv composer.phar /usr/local/bin/composer`.
      *  If you get a `permissions` error, run it again with `sudo` at the beginning. 
      *  If you get a `no such directory exists` error, run `mkdir -p /usr/local/bin`.
        *  If that gives you a `permissions` error, run with `sudo` (see the pattern?)
    1. restart terminal
  * (Windows) Stay tuned

## Laravel Package
* run `composer global require "laravel/installer"`
