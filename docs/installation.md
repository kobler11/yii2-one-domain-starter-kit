# INSTALLATION

## TABLE OF CONTENTS
- [Before you begin](#before-you-begin)
- [Manual installation](#manual-installation)
    - [Requirements](#requirements)
    - [Setup application](#setup-application)
    - [Configure your web server](#configure-your-web-server)
    - [Single domain installtion](#single-domain-installation)

- [Docker installation](#docker-installation)
- [Vagrant installation](#vagrant-installation)
- [Demo users](#demo-users)
- [Important-notes](#important-notes)

## Before you begin
1. If you do not have [Composer](http://getcomposer.org/), you may install it by following the instructions
at [getcomposer.org](http://getcomposer.org/doc/00-intro.md#installation-nix).

2. Install composer-asset-plugin needed for yii assets management
```bash
composer global require "fxp/composer-asset-plugin"
```

### Get source code
#### Download sources
https://github.com/matih/yii2-starter-kit/archive/master.zip

#### Or clone repository manually
```
git clone https://github.com/matih/yii2-one-domain-starter-kit.git
```
#### Install composer dependencies
```
composer install
```

### Get source code via Composer
You can install this application template with `composer` using the following command:

```
composer create-project --prefer-dist --stability=dev matih/yii2-one-domain-starter-kit
```

## Manual installation

### REQUIREMENTS
The minimum requirement by this application template that your Web server supports PHP 5.5.0.
Required PHP extensions:
- intl
- gd
- mcrypt



### Setup application
1. Copy `.env.dist` to `.env` in the project root.
2. Adjust settings in `.env` file
	- Set debug mode and your current environment
	```
	YII_DEBUG   = true
	YII_ENV     = dev
	```
	- Set DB configuration
	```
	DB_DSN           = mysql:host=127.0.0.1;port=3306;dbname=yii2-starter-kit
	DB_USERNAME      = user
	DB_PASSWORD      = password
	```

	- Set application relative urls
	```
	FRONTEND_URL    = /project-folder
    BACKEND_URL     = /project-folder/admin
    STORAGE_URL     = /project-folder/storage/web
	```

3. Run in command line
```
php console/yii app/setup
```

That`s all. After provision application will be accessible on http://localhost/project/folder

## Demo data
### Demo Users
```
Login: webmaster
Password: webmaster

Login: manager
Password: manager

Login: user
Password: user
```