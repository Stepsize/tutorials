# Overview

[WeChat](http://wechat.com/) is a messaging & calling app with over 300 million users. Their [API](http://dev.wechat.com/wechatapi) allows you to integrate sharing via WeChat message and [WeChat Moments](http://www.wechat.com/en/features.html#moments) into your app so your users can easily share the content (whether it's text, images, videos, links, music) with others via WeChat.

# Setup

WeChat provides iOS and Android SDKs – installing them is pretty simple, and you can find all the instructions [here](http://dev.wechat.com/wechatapi/installguide).

# Using the API

### Languages supported by Stepsize

Code snippets can be found in the Stepsize app for this API and the following languages:
- Objective-C

### Code snippets

To share any rich media from your application to WeChat, you'll need to:
  - Import & add the `WXApiDelegate` protocol
  - Create an instance of `WXMediaMessage` – the content to share
  - Send this `WXMediaMessage` via the API using `SendMessageToWXReq` with `WXSceneSession` for messages and `WXSceneTimeline` for moments

These are all the code snippets which can be retrieved via the [Stepsize](http://stepsize.com/) app:
  - [Import statements](https://gist.github.com/devStepsize/aba5498b3c760582b48bea41300ecf68) – search for `wechat import`
  - [Image](https://gist.github.com/devStepsize/43098ffc5ae71790301c10344adcf632) – search for `wechat image`
  - [Music](https://gist.github.com/devStepsize/fafbdca599972bb60cf099ca26d4d3ef) – search for `wechat music`
  - [Video](https://gist.github.com/devStepsize/ff4610de88c819e5eeb86ce3233a4e1a) – search for `wechat video`
  - [Link](https://gist.github.com/devStepsize/b8d7052abd85051f1831878027724aed) – search for `wechat link`
  - [Text](https://gist.github.com/devStepsize/682a6c18a908667c9cc135b8a62e6f94) – search for `wechat text`

Here's what this looks like in the [Stepsize](http://stepsize.com/) app:

![stepsize-app](http://i.imgur.com/6uo01MD.gif)

More details on how to use the API can be found [here](http://dev.wechat.com/wechatapi/messages-moments).

# Resources
