# Overview

This is guide provides an overview of how to get up and running with the [Twitter API](https://dev.twitter.com/overview/api) with [`node-twitter`](https://github.com/desmondmorris/node-twitter), as well as a few Node.js code snippets to perform some common operations.

# Setup

Assuming you've got a simple node server set up, install the Twitter [npm package](https://www.npmjs.com/package/twitter) by running `npm install --save twitter`.

Then register a new app with Twitter [here](https://apps.twitter.com/) or get the credentials of an existing one.

# Using the Twitter API with Stepsize

These are all the relevant code snippets which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app:
- [Require & setup the Twitter client](https://gist.github.com/devStepsize/37cefa7dd1f9caafa64fb127482a7ff6) – search for `twitter setup`
- [Retrieve the followers of a specific account](https://gist.github.com/devStepsize/8aac5877c1ecd397791c562ea0edd1de) – search for `twitter followers`
- [Connect to the Twitter stream and receive tweets matching a filter](https://gist.github.com/devStepsize/c85e2dc690b330004783d8c15b6821f5) – search for `twitter stream`
- [Create a new tweet for the authenticated account](https://gist.github.com/devStepsize/71893dc1cf09c3cca525c9c731532a08) – search for `twitter new status`​
- [Retweet a given tweet](https://gist.github.com/devStepsize/db807213ed7a0ce214ec16f95608fcd9) – search for `twitter retweet`
- [Search for tweets matching a query](https://gist.github.com/devStepsize/96f4f82b19169d9840670d6a8ca514d0) – search for `twitter search`
- [Get favourited tweets for the authenticated user](https://gist.github.com/devStepsize/c4c2f2b562d65aba75a6cc0ddad1095c) – search for `twitter favourites`
- [Send a tweet with an embedded image ](https://gist.github.com/devStepsize/8ca6df0d0d612836c8bec624561e9ba7) – search for `twitter tweet image`

# Resources

[Twitter REST API Documentation](https://dev.twitter.com/rest/public)

[Twitter Streaming API Documentation](https://dev.twitter.com/streaming/overview)

[`node-twitter` documentation](https://github.com/desmondmorris/node-twitter)
