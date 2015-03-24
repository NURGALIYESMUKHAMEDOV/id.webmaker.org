# id.webmaker.org

[![Build Status](https://travis-ci.org/mozilla/id.webmaker.org.svg?branch=master)](https://travis-ci.org/mozilla/id.webmaker.org)

OAuth 2.0 identity provider for Webmaker

## To run

Make sure you configure all necessary environment variables (see below) before running.

```
npm install
npm start
```

## Tests

To run all tests run the following command

```
npm test
```

### Front end tests

Front end tests can be run via mocha-phantom with `npm run test:browser`. You can also see the tests run in a browser if you run the app and visit `/tests`.

To add a new test, simply add it to the folder containing your component. The browser test command **automatically requires** all files matching `*.test.jsx` in the `templates/` folder.


## Environment

We haven't yet added any utilities to help load environment variables; you can do it yourself by typing in the following in your terminal:

e.g.
```
export HOST=0.0.0.0
export PORT=1234
export LOGINAPI=https://user:password@login.webmaker.org
```

You can configure the following environment variables:

```
HOST - host for this server. defaults to 0.0.0.0
PORT - port of this server, defaults to 0 (a random port above 1024)
LOGINAPI - fully qualified login.wm.org URL e.g. https://user:password@login.webmaker.org
OAUTH_DB - JSON array of oauth clients e.g.
  [{"client_id":"test","secret":"test","redirect_uri":"http://localhost:3000/account"}]
```
