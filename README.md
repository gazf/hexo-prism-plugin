# Hexo-Prism-Plugin 
[![Greenkeeper badge](https://badges.greenkeeper.io/gazf/hexo-prism-plugin.svg)](https://greenkeeper.io/)
[![wercker status](https://app.wercker.com/status/ff2e8c7215132f9a4b98ab521c76b26b/s/master "wercker status")](https://app.wercker.com/project/byKey/ff2e8c7215132f9a4b98ab521c76b26b)

Since `highlight.js` didn't support JSX syntax properly, I wrote this plugin to replace
Hexo's default code highlight plugin.

## Install
```
npm i -S gazf/hexo-prism-plugin
```
## Usage
Firstly, you should edit your `_config.yml` by adding following configuration.
```yaml
prism_plugin:
  mode: 'preprocess'    # realtime/preprocess
  theme: 'default'
  line_number: false    # default false
  custom_css: 'path/to/your/custom.css'     # optional
```
After that, check `highlight` option in `_config.yml`. Make sure that default code highlight plugin is disabled.
```yaml
highlight:
  enable: false
```
Finally, clean and re-generate your project by running following commands:

```
hexo clean
```

```
hexo generate
```

## Options
- mode:
  - realtime  (Parse code on browser in real time)
  - preprocess  (Preprocess code in node)

- theme:
  - default
  - coy
  - dark
  - funky
  - okaidia
  - solarizedlight
  - tomorrow
  - twilight
  - atom-dark
  - base16-ateliersulphurpool.light
  - cb
  - duotone-dark
  - duotone-earth
  - duotone-forest
  - duotone-light
  - duotone-sea
  - duotone-space
  - ghcolors
  - hopscotch
  - pojoaque
  - vs
  - xonokai

- line_number:
  - true (Show line numbers)
  - false (Default, Hide line numbers)

- no_assets
  - true (Stop loading asset files)
  - false (Default, load script and stylesheets files)

## Themes
You can check out prism-themes project for additional theme preview:

https://github.com/PrismJS/prism-themes#available-themes

## Supported languages
You could find the supported languages here:

http://prismjs.com/#languages-list

## License
MIT
