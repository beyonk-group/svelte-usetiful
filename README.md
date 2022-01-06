<p align="center" style="padding: 24px 0;">
  <a href="https://beyonk.com">
    <img src="https://user-images.githubusercontent.com/218949/144224348-1b3a20d5-d68e-4a7a-b6ac-6946f19f4a86.png" />
  </a>
</p>

## Svelte Usetiful

[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com) [![Svelte v3](https://img.shields.io/badge/svelte-v3-blueviolet.svg)](https://svelte.dev) [![publish](https://github.com/beyonk-adventures/svelte-usetiful/actions/workflows/publish.yml/badge.svg)](https://github.com/beyonk-adventures/svelte-usetiful/actions/workflows/publish.yml)

Svelte Product Tour using [Usetiful](https://www.usetiful.com/)

Product tours and onboarding for your application!

## Installation

```sh
pnpm i --save-dev @beyonk/svelte-usetiful
```

## Usage

Put the tour into your `__layout.svelte`.

```svelte
<!-- src/routes/__layout.svelte -->
<ProductTour token="my-usetiful-token" />

<script>
  import { Usetiful as ProductTour } from '@beyonk/svelte-usetiful'
</script>
```

### Properties

| prop | type | default | description |
| ---- | ---- | ------- | ----------- |
| `token` | string | `undefined` | Your usetiful token - required |
| `tags` | object | {} | user segmentation tags |

(See demo code for example usage.)

Updating the `tags` property will update the tags usetiful sees automatically.

## Developing

In order to run the local demo you *must* pass a valid token otherwise it won't work:

```sh
VITE_USETIFUL_TOKEN=<your-usetiful-token> pnpm run dev
```
