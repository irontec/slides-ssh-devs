# Reveal.js webpack starter

Another webpack starter for reveal.js

## Usage

Clone this proyect (delete .git folder, and push to your own remote), then change the **./content** directory:

* Edit _config.json_

* Add slides and index them on config.json (glob patterns supported!)

* Add your media files to be added on the bundle: use _assets_ folder, and use relative URLs from there.

* Edit your custom css on _content/css/index.scss_.

* Supported plugins:

  * google analitycs
  * search
  * zoom
  * menu
  * notes
  * highlightjs
  * ga

* service workers are supported with workbox.

```json
{
  "title": "🦄 Irontec reveal.js - webpack starter demo 🦄",
  "options": {
    "controls": true,
    "progress": true,
    "history": true,
    "center": true,
    "slideNumber": false,
    "touch": true,
    "hideAddressBar": true,
    "mouseWheel": true
  },
  "serviceWorker": true,
  "plugins": {
    "search": true,
    "zoom":   true,
    "menu":   true,
    "notes":  true,
    "highlightjs": true,
    "ga": "UA-XXXXXXXX-X"
  },
  "slides": [
    {"path": "index.md", "attrs": {"class":"intro"}},
    [
      "subcontent/*.md"
    ],
    "end.html"
  ]
}
```


## Development time


```bash
npm start
```

Will open a dev-server on http://localhost:8080


> If changes are made on *config.json* dev server must be *restarted*.


## Bundle time

```bash
npm run build
```

Will create a build on _./dist/_.


## Deploy time

### gitlab

There is a sample _.gitlab-ci.yaml.sample_ file to be used as a template for gitlab pipelines.

### github

There is a npm script ready for publishing on github's pages:
```bash
npm run deploy:gh
```


# TODO

* npm init command
* generate a SEO friendly dist (parse md on build time


# Instalar irontec-reveal.js-theme@0.0.4

Antes de ejecutar "npm install":

* npm set registry https://npm-packages.irontec.com
* npm adduser --registry https://npm-packages.irontec.com





