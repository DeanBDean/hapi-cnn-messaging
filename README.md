# hapi-cnn-messaging

[![NPM Package](https://img.shields.io/npm/v/hapi-cnn-messaging.svg?style=flat-square)](https://www.npmjs.org/package/hapi-cnn-messaging)
[![Build Status](https://img.shields.io/travis/cnnlabs/hapi-cnn-messaging.svg?branch=master&style=flat-square)](https://travis-ci.org/cnnlabs/hapi-cnn-messaging)
[![Coverage Status](https://img.shields.io/coveralls/cnnlabs/hapi-cnn-messaging.svg?branch=master&style=flat-square)](https://coveralls.io/github/cnnlabs/hapi-cnn-messaging)

This is a hapi.js plugin that wraps hapi-cnn-messaging to provide graceful shutdown.

The module creates an instance of messenger, that is bound to the hapi server object.

# setup

```
server.register({
    register: require('hapi-cnn-messaging'),
    options: {
        amqp: {
            connectionString: 'amqp://localhost:5672',
            exchangeName: 'EXAMPLE_APP'
        }
    }
}, (err) => {
    if (err) {
        throw err;
    }
});
```

See tests for further usage examples.

See the documentation for [cnn-messaging](http://github.com/cnnlabs/cnn-messaging) for details.
