# youkeepmeup
Pings websites. A running version is on Heroku: `youkeepmeup`.

# Deploying
It's recommended to deploy this application to an Heroku app configured with [Null Buildpack](https://github.com/ryandotsmith/null-buildpack):

```bash
$ heroku create --buildpack https://github.com/ryandotsmith/null-buildpack.git
$ git push heroku master
```

Provision the scheduler add-on:

```bash
$ heroku addons:create scheduler
```

Then, open the scheduler dashboard to add a new job:

```bash
$ heroku addons:open scheduler
```

And configure it to run as frequent as you'd like:

```bash
$ bash keepalive
```
