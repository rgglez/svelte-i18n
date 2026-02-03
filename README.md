

# svelte-i18n

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![GitHub all releases](https://img.shields.io/github/downloads/rgglez/svelte-i18n/total) 
![GitHub issues](https://img.shields.io/github/issues/rgglez/svelte-i18n) 
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/rgglez/svelte-i18n)
![Downloads](https://img.shields.io/npm/dm/@rgglez/svelte-i18n.svg)
[![npm version](https://badge.fury.io/js/svelte-i18n.svg)](https://badge.fury.io/js/@rgglez/svelte-i18n) 
![MadeWithSvelte](https://madewithsvelte.com/storage/repo-shields/2274-shield.svg)
![GitHub stars](https://img.shields.io/github/stars/rgglez/svelte-i18n?style=social)
![GitHub forks](https://img.shields.io/github/forks/rgglez/svelte-i18n?style=social)

Internationalization for Svelte.

`svelte-i18n` helps you localize your app using the reactive tools Svelte provides. By using [stores](https://svelte.dev/docs#svelte_store) to keep track of the current `locale`, `dictionary` of messages and to `format` messages, we keep everything neat, in sync and easy to use on your svelte files.

## About this fork

This fork patches a security vulnerability and updates the Svelte dependency to **version 5+**. Take this into account.

## Dependencies

- **svelte** >= 5.0.0
- **node** >= 11.15.0
- Browsers: `Chrome 38+`, `Edge 16+`, `Firefox 13+`, `Opera 25+`, `Safari 8+`.

## Usage

```javascript
<script>
  import { _ } from 'svelte-i18n'
</script>

<h1>{$_('page.home.title')}</h1>

<nav>
  <a>{$_('page.home.nav', { default: 'Home' })}</a>
  <a>{$_('page.about.nav', { default: 'About' })}</a>
  <a>{$_('page.contact.nav', { default: 'Contact' })}</a>
</nav>
```

```jsonc
// en.json
{
  "page": {
    "home": {
      "title": "Homepage",
      "nav": "Home"
    },
    "about": {
      "title": "About",
      "nav": "About"
    },
    "contact": {
      "title": "Contact",
      "nav": "Contact Us"
    }
  }
}
```

## Resources

- [Documentation / Getting Started](/docs/Getting%20Started.md)
- [Usage with Svelte Kit](/docs/Svelte-Kit.md)
- [i18n VSCode extension (3rd party)](https://github.com/antfu/i18n-ally)

## License

Original work Copyright 2017 Christian Kaisermann

This fork:

Copyright 2026 Rodolfo González González

Licenced under [MIT](https://mit-license.org/). Read the [LICENSE](LICENSE) file.
