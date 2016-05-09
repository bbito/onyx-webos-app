## enyo-dev onyx-webos-app Template for Enyo Developer Tools
> version 1.0.0

# Contents

* [Description](#description)
* [Installation](#installation)
* [Usage](#usage)

### <a name="description"></a>Description

This is a modification of the default [onyx-app template](https://github.com/enyojs/enyo-dev/tree/master/lib/enyo/lib/default-templates/onyx-app) including additional libraries: [enyo-webos](https://github.com/enyojs/enyo-webos.git) and [enyo-luneos](https://github.com/JayCanuck/enyo-luneos).

### <a name="installation"></a>Installation
```bash
# using enyo-dev you can install this remote template
enyo templates install https://github.com/bbito/onyx-webos-app.git
# init using this template
enyo init my-project -t onyx-webos-app
# set as default template
enyo templates default onyx-webos-app
```
### <a name="usage"></a>Usage

For the most part this template works like the built-in app templates and you can find out more about enyo-dev and the template system at the [enyo-dev](https://github.com/enyojs/enyo-dev) repo. It differs from the built-in templates in that it also includes a "webos-meta" directory which contains an Enyo `icon.png` and an `appinfo.json` file for use with the legacy Palm/HP webOS SDK's `palm-package` command.

* Edit the `webos-meta/appinfo.json` file to reflect your project
* Run `enyo pack`
* Copy the `icon.png` and your modified `appinfo.json` file from `webos-meta` into the `dist` directory
* Run `palm-package dist`
* Enjoy!
