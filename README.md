# :baby_chick: twitter-oauth2
[![npm version](https://badge.fury.io/js/twitter-oauth2.svg)](https://badge.fury.io/js/twitter-oauth2)
[![Build](https://github.com/kg0r0/twitter-oauth2/actions/workflows/main.yml/badge.svg)](https://github.com/kg0r0/twitter-oauth2/actions/workflows/main.yml)
[![Publish](https://github.com/kg0r0/twitter-oauth2/actions/workflows/npm.yml/badge.svg)](https://github.com/kg0r0/twitter-oauth2/actions/workflows/npm.yml)
[![CodeQL](https://github.com/kg0r0/twitter-oauth2/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/kg0r0/twitter-oauth2/actions/workflows/codeql-analysis.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Express.js middleware implementation for Twitter OAuth2 Client.

## Install
```bash
$ npm i twitter-oauth2
```

## Usage
TBD
```js
import express from 'express';
import session from 'express-session';
import { twitterOAuth2 } from 'twitter-oauth2';
const app: express.Express = express();

app.use(session({
  name: 'YOUR-SESSION-NAME',
  secret: 'YOUR-SECRET',
  cookie: {
    sameSite: 'lax'
  },
  resave: false,
  saveUninitialized: true
}))

app.use(twitterOAuth2({}))

app.get('/', (req: express.Request, res: express.Response) => {
  console.log('received tokens %j', req.session.tokenSet);
  res.send('Hello World!');
})
```

## License

[MIT](LICENSE)