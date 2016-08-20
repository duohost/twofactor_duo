Duo 2FA provider for ownCloud

Two-factor authentication (2FA) framework was added to ownCloud 9.1. This project leverages this new framework to integrate Duo 2FA into ownCloud.

Currently, some modifications to the core TwoFactorAuthentication framework were necessary, specifically to allow the Duo "iframe" to be displayed on the page, due to the default CSP restrictions. The changes are included in my fork of the ownCloud core repo: https://github.com/elie195/core

Requirements:

    - PHP 5.6 (Duo SDK requirement)
    - Duo application settings (IKEY, SKEY, HOST)
    
Installation:
    
Clone this repo to the 'apps/duo' directory of your ownCloud installation. i.e.:

    cd /var/www/html/owncloud/apps && git clone https://github.com/elie195/duo_provider.git duo
    
This has been tested on ownCloud 9.2.1 (cloned from "master" branch of the official ownCloud repo) on a CentOS 7 server with manually upgraded PHP. More detailed installation instructions to come.