# Ship-It Hubot

Ship-It is a chat bot built on the [Hubot][hubot] framework. It was
initially generated by [generator-hubot][generator-hubot], and configured to be
deployed on [Docker][Docker] to get you up and running as quick as possible. Right now it contains a fork of `plusplus`.

This README is intended to help get you started. Definitely update and improve
to talk about your own instance, how to use and deploy, what functionality is
available, etc!

[docker]: https://www.docker.com
[hubot]: http://hubot.github.com
[generator-hubot]: https://github.com/github/generator-hubot

### Running ship-it via Docker

You can start ship-it via Docker by running:

 - Build the Docker Image

`docker build -t shipit .`

 - Start a Docker Container

`docker run -d --name shipit --restart=always -e HUBOT_SLACK_TOKEN='' shipit`

What just happened?

This will run the image we just made `shipit`, as a daemon `-d`, with a default restart action of `always`, while setting an environmental variable for `HUBOT_SLACK_TOKEN` with `-e`

You'll see some start up output and a prompt:

```
npm info it worked if it ends with ok
npm info using npm@4.1.2
npm info using node@v7.7.2
npm info lifecycle ship-it@0.0.0~preinstall: ship-it@0.0.0
npm info linkStuff ship-it@0.0.0
npm info lifecycle ship-it@0.0.0~install: ship-it@0.0.0
npm info lifecycle ship-it@0.0.0~postinstall: ship-it@0.0.0
npm info lifecycle ship-it@0.0.0~prepublish: ship-it@0.0.0
npm info lifecycle ship-it@0.0.0~prepare: ship-it@0.0.0
npm info ok
[Mon Mar 13 2017 21:35:50 GMT+0000 (UTC)] INFO Logged in as <REMOVED> of <REMOVED>
[Mon Mar 13 2017 21:35:50 GMT+0000 (UTC)] INFO Slack client now connected
[Mon Mar 13 2017 21:35:50 GMT+0000 (UTC)] INFO /opt/shipit/scripts/ops.coffee is using deprecated documentation syntax
[Mon Mar 13 2017 21:35:51 GMT+0000 (UTC)] INFO hubot-redis-brain: Using default redis on localhost:6379
```
