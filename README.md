# n8n-heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/that-one-tom/n8n-heroku/tree/main)

### n8n - Free and open fair-code licensed node based Workflow Automation Tool.

This is a [Heroku](https://heroku.com/) focused container implementation of [n8n](https://n8n.io/).

Use the Deploy button above to launch n8n on Heroku. When deploying, make sure to check all configuration options and adjust them to your needs. It's especially important to set `N8N_ENCRYPTION_KEY` to a random secure value.

The default credentials for basic authentication is `user:pass`, but you should change this during the initial setup.

#### Enabling User Management

The default configuration enables basic auth as a fast and simple way to authenticate n8n users. If you prefer the more advanced user management functionality of n8n, add the variables from [this guide](https://docs.n8n.io/hosting/user-management/) to your [Heroku config vars](https://devcenter.heroku.com/articles/config-vars#using-the-heroku-dashboard).

#### Updating n8n

This requires the Heroku CLI as well as Git to be installed. You can find instructions [here](https://devcenter.heroku.com/articles/git#prerequisites-install-git-and-the-heroku-cli).

To run the upgrade, open a terminal and enter the below commands:

```
git clone https://github.com/that-one-tom/n8n-heroku.git
cd n8n-heroku
heroku git:remote -a appname # Replace app name with the actual name of your app
git push heroku main 
```

If you have previously updated n8n, you can skip both the `git clone` and `heroku git:remote` commands.