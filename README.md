# Heroku Buildpack for ReactJS app building

This repository is forked from the official [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for [Node.js apps](https://github.com/heroku/heroku-buildpack-nodejs).

[![Build Status](https://travis-ci.org/heroku/heroku-buildpack-nodejs.svg)](https://travis-ci.org/heroku/heroku-buildpack-nodejs)

## Documentation

For more information about using this Node.js buildpack on Heroku, check the [README](https://github.com/heroku/heroku-buildpack-nodejs/blob/master/README.md) from the official buildpack.

This buildpack only changes two things:
- `release` just exits instead of trying to do `npm start` (i.e. start the NodeJS app)
- after installing the node modules, the `compile` script also builds the production code by running `npm run build`.

## Tests

The buildpack tests use [Docker](https://www.docker.com/) to simulate
Heroku's Cedar-14 and Heroku-16 containers.

To run the test suite:

```
make test
```

Or to just test in cedar or cedar-14:

```
make test-cedar-14
make test-heroku-16
```

The tests are run via the vendored
[shunit2](https://github.com/kward/shunit2)
test framework.
=======
>>>>>>> [update] README.md updated with buildpack info
