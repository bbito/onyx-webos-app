## enyo-dev onyx-webos-app Template for Enyo Developer Tools
> version 1.0.1

# Contents

* [Description](#description)
* [Installation](#installation)
* [Usage](#usage)

### <a name="description"></a>Description

This is a modification of the default [onyx-app template](https://github.com/enyojs/enyo-dev/tree/master/lib/enyo/lib/default-templates/onyx-app) including additional libraries: [enyo-webos](https://github.com/enyojs/enyo-webos.git) and [enyo-luneos](https://github.com/JayCanuck/enyo-luneos). It differs from the built-in templates in that for use with the legacy Palm/HP webOS SDK's `palm-package` command, it includes 2 additonal files: an Enyo `icon.png` and an `appinfo.json` which are included in the `package.json` file's `assets` array so that they will be copied into `dist` when `enyo pack` is run. Also for legacy webOS / LuneOS support, the `ready` function in `index.js` includes 2 Palm/webOS specific lines:
```bash
ready(function () {
	window.Mojo = {relaunch: function(e) {} };
	window.PalmSystem && PalmSystem.stageReady && PalmSystem.stageReady();
	new App();
});
```

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
*IMPORTANT! The .git folder and README.md from this template repo will be copied into your project folder*
*IMPORTANT! Delete the .git folder before proceeding and either delete or remember to modify the README.md file so it describes YOUR PROJECT instead of this template*

Otherwise, for the most part this template works like the built-in app templates and you can find out more about enyo-dev and the template system at the [enyo-dev](https://github.com/enyojs/enyo-dev) repo.

* Edit the `appinfo.json` file to reflect your project
* Run `enyo pack`
* Run `palm-package dist`
* Enjoy!
