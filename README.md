# Ellac

A typography focused responsive theme for [Ghost](https://ghost.org). Ellac is based on the [Attila](https://github.com/zutrinken/attila) theme by [Peter Amende](https://github.com/zutrinken).

## Features

* [Inter](https://github.com/rsms/inter), [Fira Code](https://github.com/tonsky/FiraCode) and [System](https://github.com/jonathantneal/system-font-css) font stack
* Responsive layout
* Dark Mode
* Search
* Post reading progress
* Code highlight including line numbers
* Disqus support

## Setup [Disqus](https://disqus.com/)

1. Go to __Code injection__.
2. Add this to __Blog Header__:
````
<script>var disqus = 'YOUR_DISQUS_SHORTNAME';</script>
````

## Setup search

The search function is build with [ghostHunter](https://github.com/jamalneufeld/ghostHunter):

1. Go to __Integrations__.
2. Choose __Add custom integration__, name it `ghostHunter` and choose __Create__. Copy the generated Content API Key.
3. Go to __Code injection__.
4. Add this to __Blog Header__:
````
<script>
  var ghosthunter_key = 'PASTE_THE_GENERATED_KEY_HERE';
  //optional: set your custom ghost_root url, default is "/ghost/api/v2"
  var ghost_root_url = '/ghost/api/v2';
</script>
````
## Development

Install [Grunt](https://gruntjs.com/getting-started/):

	npm install -g grunt-cli

Install Grunt dependencies:

	npm install

Build Grunt project:

	grunt build

The `compress` Grunt task packages the theme files into `dist/ellac.zip`, which you can then upload to your site.

	grunt compress
