# youkeepmeup
Pings websites. 

# Deploying
It's recommended to deploy this application to an Heroku app configured with [Null Buildpack](https://github.com/ryandotsmith/null-buildpack):

```bash
$ heroku create --buildpack https://github.com/ryandotsmith/null-buildpack.git
$ git push heroku master
```

Then, provision the scheduler:

```bash
$ heroku addons:create scheduler
```

And configure it to run:

```bash
$ bash keepalive
```
