* Docker
* Docker Compose
* Docker Machine

* Clone this folder
* -> git clone [URL]
* -> cd [FOLDER]
* Open file [docker-compose.yml] 
*	- change 	MYSQL_ROOT_PASSWORD: password
*				MYSQL_USER: my_app
*				MYSQL_PASSWORD: secret
*				MYSQL_DATABASE: my_app
* -> docker-compose build
* -> docker-create

* Open file [docker-compose.yml]
* On Visual studio 
*	- [docker-compose.yml] right click Compose Restart
*	- Docker icon click -> right click [..._phpfpm] -> Attach Shell
*	- Install Php-composer : curl -s https://getcomposer.org/installer | php
*	- Install Cakephp : php composer.phar create-project --prefer-dist cakephp/app project