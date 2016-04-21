# Overview

No need to introduce [Slack](https://slack.com/) – you've heard of it. Let's get down to business.

With the [Slack API](https://api.slack.com/), you can create custom integrations for your own team or apps that you make available to the public. In any case, you need to start by building a custom integration, and if you want to turn it into an app, submit it to Slack to be reviewed and approved.

This tutorial provides an overview of the API and code snippets for Python using:
- [`requests`](http://docs.python-requests.org/en/master/)
- [`python-slackclient`](https://github.com/slackhq/python-slackclient)

# Setup

If you don't have a team or just want your own personal sandbox to develop in, [create a new team](https://slack.com/create).

### [Incoming Webhooks](https://api.slack.com/incoming-webhooks) – Send data into Slack in real-time

Incoming Webhooks are a simple way to post messages from external sources into Slack.
1. [Create a webhook](https://my.slack.com/services/new/incoming-webhook/)
2. POST a JSON payload to your webhook URL

Field you can send in your JSON payload:
- `text` – the message to be posted to Slack. To send a link, enclose the URL in `<>` angle brackets. To display hyperlinked text, use the pipe character like so `<https://slack.com|slack>`
- `username` – override the default identity you've set up
- `icon_emoji` – override the bot icon (e.g. `"icon_emoji": ":ghost:"`)
- `channel` – override the default channel you've set up (e.g. `"channel": "#other-channel"`)

To create richly formatted messages, see [Message formatting](https://api.slack.com/docs/formatting).

These are all the relevant code snippets which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app:
- [POST your JSON payload](https://gist.github.com/devStepsize/b1b795309a217d24566dcc0ad136f784) – search for `slack post webhook`

### [Slash Commands](https://api.slack.com/slash-commands) – Allow users to interact with external services directly from Slack

# Resources

[Message formatting](https://api.slack.com/docs/formatting) – all text in Slack uses the same system of escaping and can be richly formatted using a simple markup language similiar to Markdown
