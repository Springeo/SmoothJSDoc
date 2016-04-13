# SmoothJSDoc (based on Minami)

A clean, responsive documentation template theme for JSDoc 3.

![SmoothJSDoc Screenshot](https://raw.githubusercontent.com/remy199210/SmoothJSDoc/master/screenshots/smooth-jsdoc.png)

## Uses

- [the Taffy Database library](http://taffydb.com/)
- [Underscore Template library](http://documentcloud.github.com/underscore/#template)
- [Montserrat](http://www.google.com/fonts/specimen/Monsterrat) & Helvetica Neue
- [minami](https://github.com/nijikokun/minami)

## Install

```bash
$ npm install --save-dev smooth-jsdoc
```

## Usage

Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/smooth-jsdoc
```

### Node.js Dependency

In your projects `package.json` file add a generate script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc --configure .jsdoc.json --verbose"
}
```

In your `.jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "node_modules/smooth-jsdoc"
}
```

### Example JSDoc Config

```json
{
    "tags": {
        "allowUnknownTags": true,
        "dictionaries": ["jsdoc"]
    },
    "source": {
        "include": ["lib", "package.json", "README.md"],
        "includePattern": ".js$",
        "excludePattern": "(node_modules/|docs)"
    },
    "plugins": [
        "plugins/markdown"
    ],
    "templates": {
        "cleverLinks": false,
        "monospaceLinks": true
    },
    "opts": {
        "destination": "./docs/",
        "encoding": "utf8",
        "private": true,
        "recurse": true,
        "template": "./node_modules/smooth-jsdoc"
    }
}
```

## License

Licensed under the Apache2 license.
