# Overview

Twilio is a communication company that enables software developers to programmatically make and receive phone calls and texts using their APIs.

We'll show the important parts of the [`twilio-python`](https://github.com/twilio/twilio-python) wrapper and give some short examples of what's possible when combining this with [`Flask`](http://flask.pocoo.org/).

You can find more detailed documentation of the wrapper module [here](https://twilio-python.readthedocs.org/en/latest/).

# Setup

You can find the installation guide  [here](https://github.com/twilio/twilio-python#installation).

Basically, just run `pip install twilio`.

They say you might have to run `pip` with `sudo` but really you shouldn't.

![urgh](https://m.popkey.co/7df18a/RQXQ.gif)

Come talk to us if you need that fixed.

To get your API key, just register for an account on [Twilio's website](https://www.twilio.com/try-twilio).

# Using twilio-python

These are all the relevant code snippets which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app:
- [Set up your client with the credentials](https://gist.github.com/devStepsize/51ab73be1fc45dfe05c5e6120843a701) (grab them [here](https://www.twilio.com/user/account/settings)) - search for `twilio credentials`
- Send an [SMS](https://gist.github.com/devStepsize/be0c14b55d3d51402272e1fadd760d8f) / [MMS](https://gist.github.com/devStepsize/3a10d53033d1fd3068e0607b9c8bc517) - search for `twilio sms` or `twilio mms`
- [Make a call](https://gist.github.com/devStepsize/823d1919b37906619dd4888840dc4a79) - search for `twilio make call`
- [Modify live calls](https://gist.github.com/devStepsize/db211cf1dbbf08427f688f3c9072c746) – search for `twilio modify call`
- [Operate on call record (retrieve, delete, manipulate)](https://gist.github.com/devStepsize/4571b8edd7774acf36252260d635adff) – search for `twilio call operations`
- [TwiML syntax](https://gist.github.com/devStepsize/97bda1dd9b097ca39f929d5064186d29) - search for `twilio twiml`
- [Set up the minimal Flask server](https://gist.github.com/devStepsize/dacd467b8b7060e652e51ef5777d7c3f) - search for `flask minimal`
- [Handling incoming messages with Flask](https://gist.github.com/devStepsize/160ca2e402e0a2cce8554cb75ca9fa05) - search for `twilio flask message`
