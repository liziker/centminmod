[![GitHub stars](https://img.shields.io/github/stars/centminmod/centminmod.svg?style=flat-square)](https://github.com/centminmod/centminmod/stargazers) [![GitHub forks](https://img.shields.io/github/forks/centminmod/centminmod.svg?style=flat-square)](https://github.com/centminmod/centminmod/network) [![GitHub issues](https://img.shields.io/github/issues/centminmod/centminmod.svg?style=flat-square)](https://github.com/centminmod/centminmod/issues) [![GitHub license](https://img.shields.io/badge/license-AGPL-blue.svg?style=flat-square)](https://raw.githubusercontent.com/centminmod/centminmod/master/license.txt)

![Centmin Mod](/centmin-mod-logo2.jpg)

Centmin Mod can be installed via 2 different ways or latest install instructions on [Official Install Guide](https://centminmod.com/install.html):

1. Centmin Mod Unattended Command Line Install (highly recommended)
2. Centmin Mod installed via Git

After install bookmark and read the [Getting Started Guide](https://centminmod.com/getstarted.html) and check out the Centmin Mod Community forum at [https://community.centminmod.com](https://community.centminmod.com)

## Centmin Mod Unattended Command Line Install

Fastest method of install and allows fully unattended installation. Just type this command as root user in SSH on a fresh CentOS 6 or CentOS 7 server. Installation should take between 15-30 minutes on a fast server or up to 50-70 minutes on a slower server depending on server specs and your server's network connectivity and download speed.

### For latest 1.2.3-eva2000.08 stable install

Supports max PHP 7.0 version. For PHP 7.1+ and higher use 123.09beta01 (1.2.3-eva2000.09) beta installer below.

    yum -y update; curl -O https://centminmod.com/installer.sh && chmod 0700 installer.sh && bash installer.sh

### For latest 1.2.3-eva2000.09 beta install

Also known as 123.09beta01 branch which supports PHP 7.1, 7.2, 7.3.

default PHP 5.6 beta installer

    yum -y update; curl -O https://centminmod.com/betainstaller.sh && chmod 0700 betainstaller.sh && bash betainstaller.sh

PHP 7.0.x default beta installer

    yum -y update; curl -O https://centminmod.com/betainstaller7.sh && chmod 0700 betainstaller7.sh && bash betainstaller7.sh

PHP 7.1.x default beta installer

    yum -y update; curl -O https://centminmod.com/betainstaller71.sh && chmod 0700 betainstaller71.sh && bash betainstaller71.sh

PHP 7.2.x default beta installer

    yum -y update; curl -O https://centminmod.com/betainstaller72.sh && chmod 0700 betainstaller72.sh && bash betainstaller72.sh

PHP 7.3.x default beta installer. See [PHP 7.3 release information](https://community.centminmod.com/threads/php-7-3-0-7-2-13-7-1-25-7-0-33-5-6-39-released.16184/) and [PHP 7.3 vs 7.2 vs 7.1 vs 7.0 benchmarks](https://community.centminmod.com/threads/php-7-3-vs-7-2-vs-7-1-vs-7-0-php-fpm-benchmarks.16090/).

    yum -y update; curl -O https://centminmod.com/betainstaller73.sh && chmod 0700 betainstaller73.sh && bash betainstaller73.sh

You can also customise your installs via pre-populating the persistent config file, `/etc/centminmod/custom_config.inc` with overriding variables instead of directly editing `centmin.sh` file **BEFORE** running the the `betainstaller.sh`. See examples discussed on the forums [here](https://community.centminmod.com/threads/discussion-how-do-you-initially-install-setup-your-centmin-mod-server.14736/).

## Centmin Mod installed via Git    

Recommended way is via above curl `installer.sh` or `betainstaller.sh` commands even if you need to customise your `centmin.sh` settings - you can do that via pre-populating the persistent config file, `/etc/centminmod/custom_config.inc` with overriding variables instead of directly editing `centmin.sh` file.

Type as root user in SSH these commands, Centmin Mod will have it's install setup at /usr/local/src/centminmod. Replace `branchname=123.08stable` with `branchname=123.09beta01` if you want to install the beta version.

    yum -y install git wget nano bc unzip
    cd /usr/local/src
    branchname=123.09beta01
    git clone -b ${branchname} --depth=1 https://github.com/centminmod/centminmod.git centminmod
    cd centminmod

Then to install either type

for menu mode run centmin.sh and select menu option 1 to install

    ./centmin.sh

or for CLI install mode

    ./centmin.sh install    

## Contributing

Below are guidelines for contributing code wise. 

* [Centmin Mod Insights forum](https://community.centminmod.com/forums/centmin-mod-insights.20/) is the place to ask questions or clarifications about how Centmin Mod works under the hood.
* Every Git committed code also has a corresponding forum thread in [Centmin Mod Github.com Repo forums](https://community.centminmod.com/link-forums/centmin-mod-github-com-repository.13/) if you're more comfortable using the forums instead of the [Github issue tracker](https://github.com/centminmod/centminmod/issues).

# Bug Reports

* Bug reports can be made via [Github issue tracker](https://github.com/centminmod/centminmod/issues) or Centmin Mod official forum's [Bug Reports forums](https://community.centminmod.com/forums/bug-reports.12/).

# Pull Requests

* Pull requests can be done against the current [Github active branches](https://github.com/centminmod/centminmod/branches/active) - currently being [123.08stable](https://github.com/centminmod/centminmod/tree/123.08stable) and [123.09beta01](https://github.com/centminmod/centminmod/tree/123.09beta01). Usually once weekly, active branch changes are then merged into [master branch](https://github.com/centminmod/centminmod).

# Suggestions

* Suggestions and feedback can be made via [Github issue tracker](https://github.com/centminmod/centminmod/issues) or Centmin Mod official forum's [Feature Requests & Suggestions forums](https://community.centminmod.com/forums/feature-requests-suggestions.11/).