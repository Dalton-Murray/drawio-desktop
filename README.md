Security
--------

draw.io Desktop is designed to be completely isolated from the Internet, apart from the update process. This checks github.com at startup for a newer version and downloads it from an AWS S3 bucket owned by Github. All JavaScript files are self-contained, the Content Security Policy forbids running remotely loaded JavaScript.

No diagram data is ever sent externally, nor do we send any analytics about app usage externally. This means certain functionality for which we do not have a JavaScript implementation do not work in the Desktop build, namely .vsd and Gliffy import.

Developing
----------

**draw.io** is a git submodule of **drawio-desktop**. To get both you need to clone recursively:

`git clone --recursive https://github.com/Dalton-Murray/drawio-desktop.git`

To run this:
1. `npm install` (in the root directory of this repo)
2. `npm install` (in the drawio directory of this repo `drawio/src/main/webapp`)
3. export DRAWIO_ENV=dev if you want to develop/debug in dev mode.
4. `npm start` _in the root directory of this repo_ runs the app.

