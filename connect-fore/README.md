[![Build Status](https://travis-ci.org/pcaisse/connect-fore.svg?branch=master)](https://travis-ci.org/pcaisse/connect-fore)

# Connect "Fore!" 🏌

http://connect-fore.herokuapp.com/

## Challenge

Implement the game [Connect Four](https://en.wikipedia.org/wiki/Connect_Four) such that the source code of [game.js](static/game.js) is as short as possible without editing any other files.

## Gameplay

Gameplay is [as described here](https://en.wikipedia.org/wiki/Connect_Four#Gameplay):

* Game board is 6 x 7 (6 rows and 7 columns)
* Players alternate turns
* Player 1 is yellow; Player 2 is red
* The object of the game is to connect 4 same colored discs in a row (down, across, or diagonally)
* Play continues until a player wins

## Requirements

* Clicking on the game board will cause the disc to be "dropped" into that column
* Attempting to place a disc in a column that is full is ignored
* Upon winning, the string 'WINNER!' must be logged to the console and no further moves can be made
* No errors are thrown through normal gameplay
* Must pass all [tests](#tests)
* Must conform to the [ECMAScript 5 specification](https://www.ecma-international.org/ecma-262/5.1/)
* **No external libraries**

## Development

For development, please [install Yarn](https://yarnpkg.com/lang/en/docs/install/) and run `yarn install`.

There are several commands (see `package.json`) which are useful in development:

Command                  |Description
-------------------------|---------------------------------------------------------------------------------------------
`yarn test`              |Runs [tests](#tests)
`yarn char-count`        |Returns the number of characters in `static/game.js`
`yarn char-count-min`    |Minifies code and returns the number of characters in the minified version
`yarn compare-counts`    |Compares character count between versions of `static/game.js`
`yarn minify`            |Minifies `static/game.js`
`yarn beautify`          |Beautifies `static/game.js` (makes it more readable)
`yarn start`             |Builds and runs server
`yarn debug`             |Builds beautified version of JS for debugging and runs server
`yarn watch`             |Runs a dev build whenever the file is changed

## Tests

The test suite consists entirely of integration tests so as not to constrain the implementation in any way. For testing, a simple static file server is stood up and then UI tests are run against the code (see `test.js`).

Run tests via `yarn test`.

## Ports

`yarn start` will run a server on port 3000 by default and `yarn test` will use port 3001. To specify a different port, use the `PORT` environment variable like so:

`PORT=3333 yarn test`
