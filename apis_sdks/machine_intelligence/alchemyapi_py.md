# Overview

AlchemyAPI is machine learning API, for when you need machine brains to do the heavy lifting for you. AlchemyAPI is specialised in their Deep Learning NLP APIs which we will use here. If you want to chat more about deep learning, come talk to us.

![too.deep.](https://i.imgflip.com/12xbw1.jpg)

This tutorial provides some code snippets for Python (using the [`requests`](http://docs.python-requests.org/en/master/) library)

# Setup

It's a plain RESTful API, just get your API key from [here](http://www.alchemyapi.com/api/register.html).

Use your favourite HTTP request library to hit the endpoints. We'll be using the [`requests`](http://docs.python-requests.org/en/master/) module. You can find a quick tutorial on it [here](http://docs.python-requests.org/en/master/user/quickstart/).

Install it running `pip install requests`.


# Using AlchemyAPI

All the snippets below can be retrieved via the [Stepsize](http://stepsize.com/?ref=anvilhack) app.

## Sentiment analysis

The purpose of sentiment analysis is to determine whether a piece of text/website is positive/negative, overall or regarding a person/entity.
AlchemyAPI has a couple of tricks up its sleeves for that.

* [Basic text sentiment analysis](https://gist.github.com/devStepsize/7b96bd5c65f3abd55ce504a926688d9d) – search for `alchemyapi basic sentiment`
* [Targeted sentiment analysis](https://gist.github.com/devStepsize/cc5aaac7299fed167d80c83089e43914) – search for `alchemyapi targeted sentiment`


## Entity extraction

If you want to determine which entities are present in a text or document, you can use the following snippets

* [Text entity extraction](https://gist.github.com/devStepsize/046f082e29798d5f0bb5a30454b193fb) – search for `alchemyapi entity extraction`
* [Webpage entity extraction](https://gist.github.com/devStepsize/7c9c82f8092c88bd5cc2e558d49ea856) – search for `alchemyapi entity extraction webpage`


## Webpage clean text extraction

If you want to extract some text for modelling from a website, you will need to make sure you are not extracting rubbish. AlchemyAPI can do some smart cleaning of website to eliminate ads for example.

* [Clean text extraction](https://gist.github.com/devStepsize/74880d3e61037df9d8522aa0bb258bea) – search for `alchemyapi clean text extraction`


## Topic extraction

You might want to know which topics a website or text relates to. Use the following:

* [Topic extraction](https://gist.github.com/devStepsize/e6ed0a0b3a146e048e09e1bf4a6da70e) – search for `alchemyapi topic identification`

## Keyword extraction

To extract keywords out of a text / URL, use the following code snippets:

* [Keyword extraction from URL](https://gist.github.com/devStepsize/e0c5c516463c229f94479a439e234227) – search for `alchemyapi keyword extraction`
