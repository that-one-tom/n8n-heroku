# n8n-heroku

![Docker](https://github.com/sarveshpro/n8n-heroku/workflows/Docker/badge.svg) ![Heroku](https://github.com/sarveshpro/n8n-heroku/workflows/Heroku/badge.svg)

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

### n8n - Free and open fair-code licensed node based Workflow Automation Tool.

#### [ Open Source Contributors: Maintainers wanted! ]

This is a [Heroku](https://heroku.com/) focused container implementation of [n8n](https://n8n.io/).

Use the Deploy button above to launch n8n on Heroku. When deploying, make sure to check all configuration options and adjust them to your needs. It's especially important to set `N8N_ENCRYPTION_KEY` to a random secure value.

The default credentials for basic authentication is `user:pass`, but you should change this during the initial setup.

#### Enabling User Management

The default configuration enables basic auth as a fast and simple way to authenticate n8n users. If you prefer the more advanced user management functionality of n8n, add the variables from [this guide](https://docs.n8n.io/hosting/user-management/) to your [Heroku config vars](https://devcenter.heroku.com/articles/config-vars#using-the-heroku-dashboard).