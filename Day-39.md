## Ghost Development

### Steps

1. Install [NodeJS](http://nodejs.org/)
    This is the program that runs our server code. It installs two command line programs, `node` and `npm`.
2. Clone Ghost from https://github.com/TryGhost/Ghost.git
3. Follow the [ghost development installation guide](https://github.com/TryGhost/Ghost#getting-started-guide-for-developers)
    1. `npm install -g grunt-cli` //installs the "grunt" command on your computer
    2. `npm install` //installs all the modules that ghost depends on, listed in package.json
    3. `grunt init` (and grunt prod if you want to run Ghost in production mode) //runs a bunch of commands to build up ghost
    4. `npm start`

From here on, if you ever need to get Ghost up and running, do a `grunt dev`. This is a nifty utility that restarts the server on file change.

### Theme Development

Ghost works with two "branches" at any one time. `master`, which is where active development is occuring and which is *not* safe (ie, don't use it on a production server - your data could break) or standardized, and then a "tagged" version, which will look like `0.x.x`.

Right now, `0.4.2` is the production version of Ghost. Work is being done to move to version `0.5.0` sometime in early July.

In this class, we're going to develop themes for `0.4.2` since `0.5.0` is still up in the air. Keep in mind that if you release a theme for a certain version of Ghost, it's up to you to make sure it will work with future versions as well!