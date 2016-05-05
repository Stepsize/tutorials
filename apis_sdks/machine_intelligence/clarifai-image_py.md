# Overview

[Clarifai](https://www.clarifai.com/) is an API to understand images and videos using visual recognition technology. You can tag images and videos by content, find similar images using image queries.

The full API documentation can be found [here](https://developer.clarifai.com/guide/).

This tutorial describes how to get setup with [Clarifai's Python client](https://github.com/Clarifai/clarifai-python) `clarifai-python` to use the <b>image tagging API</b>.

It lets you tag pictures like so:

`performance` `concert` `music` `stage`

![Concert](http://i.imgur.com/BflW5HQ.jpg)

# Setup

- Sign up to the Clarifai API [here](https://developer.clarifai.com/signup/)
- Verify your email address
- Create an application on the sign up welcome screen or [here](https://developer.clarifai.com/account/applications/) if you (also) hate their forced default application name...
- Install [`clarifai-python`](https://github.com/Clarifai/clarifai-python) by running `pip install git+git://github.com/Clarifai/clarifai-python.git` in your terminal
- Export your application Client Id & Client Secret which can be found on your [application's page](https://developer.clarifai.com/account/application) by running these two commands in your terminal
  - `export CLARIFAI_APP_ID=<an_application_id_from_your_account>`
  - `export CLARIFAI_APP_SECRET=<an_application_secret_from_your_account>`
- The client might recommend installing [Pillow](https://pillow.readthedocs.io/en/latest/installation.html). If so, run `pip install Pillow`.

You're good to go.

# Using the API in Python

The relevant code snippets which can be retrieved via the [Stepsize](http://stepsize.com/?ref=anvilhack) app can be found here. It's all you need for image tagging:
- [Tag a list of local images](https://gist.github.com/devStepsize/b76fa99db3c1962be7372f08e71a158c) – search for `clarifai python image local`
- [Tag a list of public images](https://gist.github.com/devStepsize/a1ecd3538a632a4446ffb1c9f6627bc4) – search for `clarifai python image url`
