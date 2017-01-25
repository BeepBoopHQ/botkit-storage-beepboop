[![Sponsored by Beep Boop](https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F_sponsored_by-%E2%9C%A8_Robots%20%26%20Pencils%20%2F%20Beep%20Boop_%E2%9C%A8-FB6CBE.svg)](https://beepboophq.com)

# botkit-storage-beepboop
Storage module for Botkit when running on [Beep Boop][beepboop].  Internally this module uses the BeepBoop [Persist API](https://beepboophq.com/docs/article/api-persist) along with the [Slack Teams API](https://beepboophq.com/docs/article/api-slack-teams) to provide a Botkit storage adapater.

## Install

```bash
npm install --save botkit-storage-beepboop
```

## Usage

This module expects the following environment variable to be set for authentication.  It's set automatically when running on Beep Boop, but when running locally you need to make sure you set it appropriately.

```bash
BEEPBOOP_TOKEN="API_TOKEN_FROM_BEEPBOOP_PROJECT"
```

```js
var BotkitStorageBeepBoop = require('botkit-storage-beepboop')

var controller = Botkit.slackbot({
  storage: BotkitStorageBeepBoop()
})
```

## BotkitStorageBeepBoop([options])
Returns a Beep Boop Perist api:

+ `options.token` - defaults to `process.env.BEEPBOOP_TOKEN` - auth token passed into environment by Beep Boop
+ `options.url` - defaults to `process.env.BEEPBOOP_API_URL || 'https://beepboophq.com/api/v1` - api url passed into environment by Beep Boop

[beepboop]: https://beepboophq.com
