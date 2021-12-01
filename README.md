<p align="center">
  <a href="https://beyonk.com">
    <img width="186" height="90" src="https://user-images.githubusercontent.com/218949/144224348-1b3a20d5-d68e-4a7a-b6ac-6946f19f4a86.png" />
  </a>
</p>

## Svelte Usetiful

[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com) [![Svelte v3](https://img.shields.io/badge/svelte-v3-blueviolet.svg)](https://svelte.dev)

Svelte Usetiful integration

[https://www.usetiful.com/](https://www.usetiful.com/)

Product tours and onboarding for your application!

## Installation

```sh
pnpm i --save-dev @beyonk/svelte-usetiful
```

## Usage

```svelte
<!-- src/routes/__layout.svelte -->
<ProductTour token="my-usetiful-token" />

<script>
  import ProductTour from '@beyonk/svelte-usetiful'
</script>
```

### Properties

| prop | type | default | description |
| ---- | ---- | ------- | ----------- |
| `token` | string | `undefined` | Your usetiful token - required |
| `segment` | string | `undefined` | segment my users |
| `language` | string | `undefined` | target specific languages |
| `role` | string | `undefined` | target specific user roles |
| `firstName` | string | `undefined` | personalize my content |

(See demo code for example usage.)

## Developing

In order to run the local demo you *must* pass a valid token otherwise it won't work:

```sh
VITE_USETIFUL_TOKEN=<your-usetiful-token> pnpm run dev
```
