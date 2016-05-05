# Overview

[Clarifai](https://www.clarifai.com/) is an API to understand images and videos using visual recognition technology. You can tag images and videos by content, find similar images using image queries.

The full API documentation can be found [here](https://developer.clarifai.com/guide/).

This tutorial describes how to get setup with [Clarifai's Node.js client](https://github.com/Clarifai/clarifai-nodejs/) `clarifai-nodejs` to use the <b>image tagging API</b>.

It lets you tag pictures like so:

`performance` `concert` `music` `stage`

![Concert](http://i.imgur.com/BflW5HQ.jpg)

# Setup

- Sign up to the Clarifai API [here](https://developer.clarifai.com/signup/)
- Verify your email address
- Create an application on the sign up welcome screen or [here](https://developer.clarifai.com/account/applications/) if you (also) hate their forced default application name...
- Download this [file](https://github.com/Clarifai/clarifai-nodejs/blob/master/clarifai_node.js) and drop it into your project (at the root or elsewhere)
- Export your application Client Id & Client Secret which can be found on your [application's page](https://developer.clarifai.com/account/application) by running these two commands in your terminal
  - `export CLARIFAI_APP_ID=<an_application_id_from_your_account>`
  - `export CLARIFAI_APP_SECRET=<an_application_secret_from_your_account>`

You're good to go.

# Using the API in Node.js

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=anvilhack) app can be found here. It's all you need for image tagging:
- [Tag a list of public images](https://gist.github.com/devStepsize/bd80d97245e761629d3058f8eebf8f21) – search for `clarifai node image url`
