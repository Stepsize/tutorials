# Overview

No need to introduce [Slack](https://slack.com/) – you've heard of it. Let's get down to business.

With the [Slack API](https://api.slack.com/), you can create custom integrations for your own team or apps that you make available to the public. In any case, you need to start by building a custom integration, and if you want to turn it into an app, submit it to Slack to be reviewed and approved.

Here's what you can do with the API:
- Send data into Slack in real-time with [Incoming Webhooks](#incoming-webhooks--send-data-into-slack-in-real-time)
- Allow users to interact with external services directly from Slack with [Slash Commands](#slash-commands--allow-users-to-interact-with-external-services-directly-from-slack)
- Get data out of Slack in real-time with [Outgoing Webhooks](#outgoing-webhooks--get-data-out-of-slack-in-real-time)
- Interact with Slack in more complex ways with the Web API (e.g. manipulate channels, files, etc.)
- Create bot users with the Real Time Messaging API

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

Slack provides a really simple client called `python-slackclient` to use the API in Python. Install it by runnning `pip install slackclient`.

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app is:
- [Call the Web API](https://gist.github.com/devStepsize/3a88cecceb3556c45829bc5388a150ee) with `python-slackclient` – search for `slack web api`

### [Real Time Messaging API](https://api.slack.com/rtm) – WebSocket-based API to receive events from Slack in real time and send messages as users

To be added

# Resources

[Message formatting](https://api.slack.com/docs/formatting) – all text in Slack uses the same system of escaping and can be richly formatted using a simple markup language similiar to Markdown

[Widely-used open source libraries](https://api.slack.com/community)
