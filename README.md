<h1 align='center'>
  kPointPlayer
</h1>

<p align='center'>
  <a href='https://www.npmjs.com/package/react-player'>
    <img src='https://img.shields.io/npm/v/react-player.svg' alt='Latest npm version'>
  </a>
  <a href='https://travis-ci.org/CookPete/react-player'>
    <img src='https://img.shields.io/travis/CookPete/react-player/master.svg' alt='Build Status'>
  </a>
  <a href='https://codecov.io/gh/CookPete/react-player'>
    <img src='https://img.shields.io/codecov/c/github/cookpete/react-player.svg' alt='Test Coverage'>
  </a>
  <a href='https://www.patreon.com/cookpete'>
    <img src='https://img.shields.io/badge/sponsor-patreon-fa6854.svg' alt='Become a sponsor on Patreon'>
  </a>
</p>

<p align='center'>
  A React component for embeding video in kpoint player. 
</p>

### Migrating to ReactPlayer `v2.0`

ReactPlayer `v2.0` changes single player imports and adds lazy loading players. Support for `preload` has also been removed, plus some other changes. See [`MIGRATING.md`](/MIGRATING.md) for information.

### Usage

```bash
npm install aditya-kpoint-player
```

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import KpointPlayer from './lib/components/KpointPlayer'

ReactDOM.render(
  <React.StrictMode>
    <KpointPlayer domain="ktpl.kpoint.com"
    videoId="gcc-d9e8dbc3-5dfa-4f68-bf7a-97f25fb7632c"
    height="360px"
    width="640px"
    offset="50000"
    hide="search, toc, logo"
    resume="false"  
    />
  </React.StrictMode>,
  document.getElementById('root')
);

```
For platforms without direct use of `npm` modules, a minified version of `ReactPlayer` is located in `dist` after installing. To generate this file yourself, checkout the repo and run `npm run build`.

## Props

Prop | Description | Default
---- | ----------- | -------
`domain` | Host name of your kPoint server. Typically of the form acme.kpoint.com. | `""`
`vidoeId` | Id of the video to load. | `""`
`width` | Set the width of the player | `640px`
`height` | Set the height of the player | `360px`
`style` | Add [inline styles](https://facebook.github.io/react/tips/inline-styles.html) to the root element | `{}`
`offset` | Start offset in milliseconds to start the video from
`hide` | You can choose to hide a certain player controls based on the use case. Here is a list of supported controls which can be hidden. | `{}`
`xt` | Xauth token. Please see developer console for info on how to generate and use Xauth token.
`resume` | Do not show options to resume video from last position | `false`
`cookie_name` | Tracks the cookie with the provided name. 


