# n8n-heroku

![Docker](https://github.com/sarveshpro/n8n-heroku/workflows/Docker/badge.svg) ![Heroku](https://github.com/sarveshpro/n8n-heroku/workflows/Heroku/badge.svg)

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/sarveshwarge/n8n-heroku)

#### [ Open Source Contributors feel free to maintain this repository ]

Use the Deploy button above to launch n8n on Heroku. Make sure to check all configuration options and adjust them to your needs. It's especially important to set `N8N_ENCRYPTION_KEY` to a random secure value.

Also, now set app stack to container and simply connect this Github repo and deploy, heroku uses default configuration from app.json

default basic auth is user:pass

### Free and open fair-code licensed node based Workflow Automation Tool.

This is a [Heroku](https://heroku.com/) focused container implementation for the [n8n Automation Tool](https://n8n.io/). Just connect your fork to heroku and let it work as a charm!


## Using Container Registry

you can also deploy this project using container registry (requires aditional requirements installed). Just clone/download this repository on your local machine.

### Additional Requirements (for building on local)
* docker
* docker-compose

### Steps
cd into your project directory

    cd n8n-heroku/

login into heroku account
    
    heroku login

create heroku app

    heroku create APP_NAME

change app stack

    heroku stack:set container --app APP_NAME
    
set config vars(optional)

    heroku config:set N8N_BASIC_AUTH_ACTIVE=true
    heroku config:set N8N_BASIC_AUTH_USER=SET_USERNAME
    heroku config:set N8N_BASIC_AUTH_PASSWORD=SET_PASSWORD

Login the container

    heroku container:login

build and push container image to heroku

    heroku container:push web --app APP_NAME
    
release new build

    heroku container:release web --app APP_NAME
    
<br />

Maybe now you can specify which N8N version to install by Setting a Environment Variable N8N_VERSION or with a build time argument of the same. Not tested yet though, create an issue if it does't work. CI is passing so it is working correctly with default values.

_Update - To set n8n version you can pass a argument when deploying using container registry_

    heroku container:push web --arg N8N_VERSION=0.60.0 --app APP_NAME

### Sources

https://github.com/n8n-io/n8n
