# Overview

IBM Watson is our favourite Jeopardy-playing AI. They have some cool experimental & beta Machine Learning services. We'll showcase their 'tone analyser', which is the best way at the moment to detect your snarky passive aggressive comments.

# Setup

1. Sign-up [here](https://console.ng.bluemix.net/registration/?Target=https%3A%2F%2Fconsole.ng.bluemix.net%2Flogin)
2. Log in. (Your IBM id is just your email)
3. You will land on your dashboard page, click on Services and API and select the Tone analyser.
4. Give it any name you want (`anvil-hack` maybe?) and create the service.
5. Go to service credentials and get them.

# Using the API

We'll show you how to use the API using the [Requests](http://docs.python-requests.org/en/master/) library for Python.

To perform an analysis of a piece of text, use the following snippet:

* [Tone analysis of a given text](http://gist.github.com/a215918ceda27dbe9b025fd6d85565b1)
