# VSG

A lightweight, atomic and reusable CSS framework and style guide.
      
## Getting Started

You'll need

- [**git** `v2.7.x`](https://git-scm.com/)
- [**Node.js** `v4.4.x`](http://nodejs.org/download/)
- [**npm** `v3.8.x`](https://docs.npmjs.com/getting-started/installing-node#updating-npm) - just run `sudo npm install -g npm` after installing Node.js
- [sass](http://sass-lang.com/install)
- [scss-lint](https://github.com/brigade/scss-lint)

To start, clone `vsg`

``` bash
cd ~/workspace
git clone git@github.com:HenrikR/vsg.git
cd vsg
```

Install the dev dependencies.

``` bash
npm install
```

Watch files for compilation.
``` bash
npm start
```

Start building!
``` bash
code src/app.scss
```

## Builds
Create a minified build.
``` bash
npm run build
```

## Docs

For documentation and preview of your build, please run and open the docs in a browser.
``` bash
npm run docs
```

## Development

### Manifesto

This is a guide to the available styles in the application.
Here is a general outline and key of good things to know:

- Styles are <strong>mobile first</strong> &mdash; so consider making them lightweight and perform well

- Styles use <strong>a namespace</strong> &mdash; prefix them with: <strong class="v-code">v-</strong>

- Styles are <strong>atomic</strong> &mdash; designed to handle a specific thing: <strong class="v-code">-p for padding, -m for margin, -b for border, ...</strong>

- Styles are <strong>responsive</strong> &mdash; each style can be extended to target devices using a prefix of: <strong class="v-code">-s- -m- -l-</strong>

- Styles are <strong>concise</strong> &mdash; by limiting variations using a common scale: <strong class="v-code">-1 -2 -3 -4</strong>


### Settings

The current settings used are:

- <strong class="v-code v-mr2">v-&lt;style&gt;1</strong> 0.625rem or 10px
- <strong class="v-code v-mr2">v-&lt;style&gt;2</strong> 1.25rem or 20px
- <strong class="v-code v-mr2">v-&lt;style&gt;3</strong> 2.5rem or 40px
- <strong class="v-code v-mr2">v-&lt;style&gt;4</strong> 3.75rem or 60px
- <strong class="v-code v-mr2">v-s-&lt;style&gt;</strong> 35.5em and above or >= 568px
- <strong class="v-code v-mr2">v-m-&lt;style&gt;</strong> 64em and above or >= 1024px
- <strong class="v-code v-mr2">v-l-&lt;style&gt;</strong> 79.875em and above or >= 1278px


### Themes

Creating additional themes within the framework is intended to be straightforward and simple.

Start by creating a new theme name (use a descriptive name, try not to base it on a color)

``` bash
src/themes/<nightlife>
```

Create a similar configuration file from `src/_config.scss`.

``` bash
src/themes/<nightlife>/_config.scss
```

Select the components and styles you wish to theme. For example:

``` bash
src/themes/<nightlife>/colors.scss
```

The configuration of the theme will do the heavy lifting in overriding the framework and components styles.

When ready, include the theme in the app's styles.

``` css
@import 'themes/<nightlife>/theme';
```

And apply the theme name to the containing element.

```html
<div class="v-nightlife">
```
