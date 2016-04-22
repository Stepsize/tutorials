# Overview

Twilio is a communication company that enables software developers to programmatically make and receive phone calls and texts using their APIs.

We'll show the important parts of the [`twilio-python`](https://github.com/twilio/twilio-python) wrapper. And give some short examples of what's possible when combining this and [`Flask`](http://flask.pocoo.org/).

You can find more detailed documentation of the wrapper module [here](https://twilio-python.readthedocs.org/en/latest/)

# Setup

You can find the installation guide  [here](https://github.com/twilio/twilio-python#installation).

Basically, just run `pip install twilio`.

They say you might have to run `pip` with `sudo` but really you shouldn't.

![urgh](https://m.popkey.co/7df18a/RQXQ.gif)

Come talk to us if you need that fixed.

To get your API key, just register for an account on Twilio's website, they have a hackathon's tier.

# Using twilio-python

Code snippets can be found in the [Stepsize](http://www.stepsize.com/?ref=hacksussex) app for this API. We're be using [flask](http://flask.pocoo.org/) for the server implementation.

## Code snippets

### Credentials

On your [account's page](https://www.twilio.com/user/account/settings) grab your credentials and save them somewhere (safe).

* Set up your client with the credentials - search for `twilio credentials`

### Sending messages/SMS/MMS



* Sending an SMS - search for `twilio sms`

### Making a phone call
* Making a call - search for `twilio call`

### TwiML basics
* TwiML syntax - search for `twilio twiml`

### Simple Flask examples

* Set up the minimal Flask server - search for `flask minimal`

* Handling incoming messages with Flask - search for `twilio flask message`
