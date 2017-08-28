# Development Environment Setup

## Get [AWS](https://aws.amazon.com) (free tier) or DigitalOcean (student discount from [GitHub](https://education.github.com))

- Make sure the virtual machine has the **Ubuntu 16.04** operating system.  This should be the default OS on both services. 

## On the **Ubuntu 16.04** Virtual Machine

- `mkdir -p ~/web4350`
- `cd ~/web4350`
- `sudo apt install unzip php7.0 php-mbstring php-soap php-xml php-zip`
- Goto page [https://getcomposer.org/download](https://getcomposer.org/download/)
- Run this in your console:
```sh
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
- Goto page [https://getcomposer.org/doc/00-intro.md#globally](https://getcomposer.org/doc/00-intro.md#globally)
- `sudo mv composer.phar /usr/local/bin/composer`
- Run this in your console:
```sh
git config --global user.name "<github username>"
git config --global user.email "<github email>"
```
- `cd ~`
- `touch .netrc`
- `vim .netrc`
- Contents of the `.netrc` file should be:
```sh
machine github.com
  login <github username>
  password <github application token>
```
