# Run-Composer-version1-2-simultaneously

1. Install Composer globally, following the instructions from https://getcomposer.org/doc/00-intro.md#installation-linux-unix-macos. This will install the latest Composer 2 version in /usr/local/bin. (on Mac you can simply run brew install composer)
2. Move composer to composer2: mv /usr/local/bin/composer /usr/local/bin/composer2
3. CD to the /usr/local/bin/ folder: /usr/local/bin/
   4.Download the latest V1 version from https://getcomposer.org/download/1.10.17/composer.phar : wget https://getcomposer.org/download/1.10.17/composer.phar
   5.Make the downloaded phar file executable: chmod 755 composer.phar
   6.Rename composer to composer1: mv /usr/local/bin/composer.phar /usr/local/bin/composer1
   7.Now create a symlink for the global version you want to use: ln -s /usr/local/bin/composer1 /usr/local/bin/composer. If you are using a local PHP switcher like dnsmasq or valet, make sure to use composer1 as your global Composer version - otherwise you will get Composer errors if you are on PHP < 7.2.0. If you never run PHP < 7.2.0 locally, you should use Composer 2 as your default.
   8.To use global Composer: run composer --version
   9.To use global Composer 1: run composer1 --version
   10.To use global Composer 2: run composer2 --version
