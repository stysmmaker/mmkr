# mmkr
_It's just my handle but shorter_

> This project was created thanks to the help of [create-expression-lib](https://github.com/motiondeveloper/create-expression-lib)!

## Overview

This expressions library is mostly a collection of tools I find personally useful. Some pertain to general tasks and others more specific, i.e. YTPMV/音MAD.

## Usage

1. Download the latest version of `mmkr.jsx` from the releases page.
2. Import `mmkr.jsx` into your After Effects project.
3. Reference the library in your expressions like so:

```js
const MMKR = footage('mmkr.jsx').sourceData.get_functions();
```

Functions will now be usable from the `MMKR` object:
```js
const MMKR = footage('mmkr.jsx').sourceData.get_functions();
MMKR.inertial_bounce(5, 2, 4); // Apply a bounce to the current property
```

You can also destructure the returned object:
```js
const { inertial_bounce } = footage('mmkr.js').sourceData.get_functions();
inertial_bounce(5, 2, 4);
```

## Development

```sh
git clone repoUrl.git
cd mmkr

# Automatically refresh .jsx output file
npm run watch

# Once off build
npm run build

# Distribute release
npm run release
```