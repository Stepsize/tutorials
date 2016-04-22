# Overview

No need to introduce [Slack](https://slack.com/) – you've heard of it. Let's get down to business.

With the [Slack API](https://api.slack.com/), you can create custom integrations for your own team or apps that you make available to the public. In any case, you need to start by building a custom integration, and if you want to turn it into an app, submit it to Slack to be reviewed and approved.

Here's what you can do with the API:
- Send data into Slack in real-time with [Incoming Webhooks](#incoming-webhooks--send-data-into-slack-in-real-time)
- Allow users to interact with external services directly from Slack with [Slash Commands](#slash-commands--allow-users-to-interact-with-external-services-directly-from-slack)
- Get data out of Slack in real-time with [Outgoing Webhooks](#outgoing-webhooks--get-data-out-of-slack-in-real-time)
- Interact with Slack in more complex ways with the [Web API](#web-api--interact-with-slack-in-more-complex-ways) (e.g. manipulate channels, files, etc.)
- Create bot users with the [Real Time Messaging API](#real-time-messaging-api--websocket-based-api-to-receive-events-from-slack-in-real-time-and-send-messages-as-users)

This tutorial provides an overview of the API and code snippets for Python using:
- [`requests`](http://docs.python-requests.org/en/master/)
- [`flask`](http://flask.pocoo.org/)
- [`python-slackclient`](https://github.com/slackhq/python-slackclient)

# Setup

If you don't have a team or just want your own personal sandbox to develop in, [create a new team](https://slack.com/create).

### [Incoming Webhooks](https://api.slack.com/incoming-webhooks) – Send data into Slack in real-time

Incoming Webhooks are a simple way to post messages from external sources into Slack.

1. [Create a webhook](https://my.slack.com/services/new/incoming-webhook/)
2. [POST a JSON payload](https://gist.github.com/devStepsize/b1b795309a217d24566dcc0ad136f784) to your webhook URL

These are all the relevant code snippets which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app:
- [POST your JSON payload](https://gist.github.com/devStepsize/b1b795309a217d24566dcc0ad136f784) – search for `slack post webhook`
- [List of the JSON fields](https://gist.github.com/devStepsize/f7e856e9680eb82e03b4351ec1b42c81) – search for `slack webhook fields`

To create richly formatted messages, see [Message formatting](https://api.slack.com/docs/formatting).

### [Slash Commands](https://api.slack.com/slash-commands) – Allow users to interact with external services directly from Slack

Messages that start with a slash `/` are commands and will behave differently from regular messages – they're used to interact with external services.

1. Create a custom command [here](https://my.slack.com/services/new/slash-commands)
2. Implement your server-side logic to respond to the command
  - If the request fails validation, respond with a HTTP status code other than `200`
  - Otherwise, you can respond with plain text and a HTTP `200` status code
  - Or you can respond with a JSON payload and a HTTP `200` status code
  - Or you can send up to 5 responses (optionally delayed by up to 30 minutes) by POSTing JSON payloads to the `response_url` included in the command request data

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app is:
- [Handle slash commands with Flask](https://gist.github.com/devStepsize/59c15d850e82a77e539b8ff3d5cb5cad) – search for `slack slash command`

Custom commands for your own team have almost no restrictions (HTTPS support with valid SSL certificate), but if you aim to share your commands as Slack apps there are some [additional restrictions](https://api.slack.com/slash-commands).

### [Outgoing Webhooks](https://api.slack.com/outgoing-webhooks) – Get data out of Slack in real-time

This integration is only available in public channels. Outgoing webhooks will run on messages sent to Slack when one or both of the following are true:
- The message is in the specified channel
- The message begins with one of the defined trigger word(s)

When a chat message is received that matches the conditions, a JSON payload will be POSTed to all of the URLs defined.

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app is:
- [Handle outgoing webhook with Flask](https://gist.github.com/devStepsize/6b5f970c5d910e5bad5f76d2a2812caa) – search for `slack outgoing webhook`

### [Web API](https://api.slack.com/web) – Interact with Slack in more complex ways

Slack's web API exposes a bunch of methods to interact with Slack in more complex ways – e.g. manipulate channels & files, create reminders, etc. The full list of API methods can be found [here](https://api.slack.com/methods).

Slack provides a really simple client called [`python-slackclient`](https://github.com/slackhq/python-slackclient) to use the API in Python. Install it by runnning `pip install slackclient`.

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app is:
- [Call the Web API](https://gist.github.com/devStepsize/3a88cecceb3556c45829bc5388a150ee) with [`python-slackclient`](https://github.com/slackhq/python-slackclient) – search for `slack web api`

### [Real Time Messaging API](https://api.slack.com/rtm) – WebSocket-based API to receive events from Slack in real time and send messages as users

The Real Time Messaging API is a WebSocket-based API that allows you to receive events from Slack in real time and send messages as users.

If you're not familiar with WebSocket, check [wikipedia](https://en.wikipedia.org/wiki/WebSocket) – basically it allows you to open a bi-directional communication channel between two apps and keep it open while you do your thing and data flows back and forth between the two apps.

Slack's [`python-slackclient`](https://github.com/slackhq/python-slackclient) makes this ridiculously simple. If you need to, install it by runnning `pip install slackclient`.

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app is:
- [Using the Real Time Messaging API](https://gist.github.com/devStepsize/b37376c8263a02359401e6f0c155a3ea) with [`python-slackclient`](https://github.com/slackhq/python-slackclient) – search for `slack real time api`

The list of all event types which Slack may send to your app as well as the messages your can send to Slack can be found [here](https://api.slack.com/rtm).

#### Building Bots with the RTM API

See [python-rtmbot](https://github.com/slackhq/python-rtmbot/) for an active project using the Real Time Messaging API with [`python-slackclient`](https://github.com/slackhq/python-slackclient).

If you're planning to use the Real Time Messaging API to create a bot, you'll want to read this [documentation](https://api.slack.com/bot-users). You'll want to connect to the API using your bot user's OAuth token, awarded to you a when team authorises your application. Create a bot user [here](https://my.slack.com/services/new/bot).

Note: if you're familiar with Node.js, you might want to consider using [Botkit](https://howdy.ai/botkit/) to create your bot – the framework takes care of most of the API gymnastics.

# Resources

[Message formatting](https://api.slack.com/docs/formatting) – all text in Slack uses the same system of escaping and can be richly formatted using a simple markup language similiar to Markdown

[Widely-used open source libraries](https://api.slack.com/community)

[How to write a Slack bot end-to-end using Python and `python-slackclient`](https://medium.com/@julianmartinez/how-to-write-a-slack-bot-end-to-end-d6a8542c854b#.f04moiyf5)
