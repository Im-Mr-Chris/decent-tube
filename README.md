
# PolyTube App

A decentralized version of YouTube on the Polygon Network.

## Preview

## Install

### Install Meteor
* Linux and Mac: `curl https://install.meteor.com/ | sh`
* Windows: [link](https://www.meteor.com/install)

### Install the app

Clone this repository and `meteor npm install` in it. This will install all dependencies coming from npm including the ones required for development.

### Start the app
Finally, do `meteor` in the folder to start the app in development mode.


##### Options:
* `-p 3456` for running on a different port than the default 3000.
* `--production` will minify and merge the javascript and css files.

Meteor will automatically push any change on the code to the browser while you keep the meteor dev server running.

## Going in-depth
### Running blockchain locally
You can run a blockchain locally on your PC to avoid sending transactions onto the live network. Follow instructions in [dtube/avalon](https://github.com/dtube/avalon), then just change API to 'localhost:3001' in the settings page to point your UI to your development chain.

### Working with Uploads

For doing anything on the upload side, it is strongly recommended to run your own [dtube/ipfs-uploader](https://github.com/dtube/ipfs-uploader). Once running, simply turn the `localhost` setting to `true` in `client/settings.js` and it will upload locally instead of our production servers.

## Structure

 - `.meteor` meteor files, don't touch unless you know what you are doing.
 - `.vscode` if you use visual studio code.
 - `public` all the static files like pictures, fonts and translations.
 - `client` all the app code
 - - `client/collections` minimongo collections that templates feed from
 - - `client/css` css files.
 - - `client/lib` semantic ui related code.
 - - `client/views` templates, each has 2 files, html and js, a handlebar template and associated logic.
 - - - `client/views/commons` all the re-used templates
 - - - `client/views/pages` all the templates matching a route in `router.js`
 - - - `client/views/topbar` the fixed menu on top of the app
 - - - `client/views/sidebar` the sidebar menu

## Common Issues

If you are using windows, the `meteor npm` seems to be buggy at times. You can try using the normal `npm` instead if you have that installed.

After each meteor or package.json update, you will need to re-run `meteor npm install`
