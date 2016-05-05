# Overview

The [Azure Face API](https://www.microsoft.com/cognitive-services/en-us/face-api) allows you to do funky things like detect faces in images and get details about facial features, group faces based on similarity, etc.

This tutorial covers detecting faces in image(s) using the python [`requests`](http://docs.python-requests.org/en/master/) library.

# Setup

- Create a Microsoft account [here](http://account.windowsazure.com) (if you don't have one). You'll need to enter your debit card details, but the API has a free tier and you won't be charged without manually upgrading your access level
- Select the Face API preview access when creating your account (or [here](https://www.microsoft.com/cognitive-services/en-US/subscriptions) after signing up)
- Find your API key on your [account page](https://www.microsoft.com/cognitive-services/en-US/subscriptions) (Key 1 in Face-Preview)
- `pip install requests` if needed

# Using the API in Python

The relevant code snippets which can be retrieved via the [Stepsize](http://stepsize.com/?ref=anvilhack) app can be found here. It's all you need for face detection:
- [Detect faces in a local image](http://gist.github.com/f815abf224953a72253cb73fb44e933a) – search for `azure face local image`
- [Detect faces in a public image](https://gist.github.com/devStepsize/57e863679776b9ab896ab377d1179599) – search for `azure face public image`
