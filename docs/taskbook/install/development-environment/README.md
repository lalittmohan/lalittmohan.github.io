### Requirements

- Setup already project in local machine from repository(gibhut|gitlab|bitbucket)

####MacOS:

Install Docker, Docker-compose and Docker-sync.

####Windows:

Install Docker, Docker-compose and Docker-sync.

####Linux:

Install Docker and Docker-compose.

> Prerequisite =>  warden installed  
> [Installation Guide Documentation](https://docs.warden.dev/)

``mkdir -p ~/Sites/exampleproject``

``cd ~/Sites/exampleproject``

``warden env-init exampleproject magento2``

Its Create ``.env`` file in project root folder
> commit this to your VCS to share the configuration with other team members

```yaml
WARDEN_ENV_NAME=exampleproject // project name
WARDEN_ENV_TYPE=magento2
WARDEN_WEB_ROOT=/

TRAEFIK_DOMAIN=exampleproject.test // project url 
TRAEFIK_SUBDOMAIN=app  // optional

WARDEN_DB=1   
WARDEN_ELASTICSEARCH=1
WARDEN_VARNISH=1
WARDEN_RABBITMQ=1
WARDEN_REDIS=1

WARDEN_SYNC_IGNORE=

ELASTICSEARCH_VERSION=7.6
MARIADB_VERSION=10.3
NODE_VERSION=12
COMPOSER_VERSION=1
PHP_VERSION=7.3
PHP_XDEBUG_3=1
RABBITMQ_VERSION=3.8
REDIS_VERSION=5.0
VARNISH_VERSION=6.0

WARDEN_ALLURE=0
WARDEN_SELENIUM=0
WARDEN_SELENIUM_DEBUG=0
WARDEN_BLACKFIRE=0
WARDEN_SPLIT_SALES=0
WARDEN_SPLIT_CHECKOUT=0
WARDEN_TEST_DB=0
WARDEN_MAGEPACK=0

BLACKFIRE_CLIENT_ID=
BLACKFIRE_CLIENT_TOKEN=
BLACKFIRE_SERVER_ID=
BLACKFIRE_SERVER_TOKEN=
```

``warden sign-certificate exampleproject.test``

``warden env up``

drop into shell withing project environment command run from php-fpm docker container

