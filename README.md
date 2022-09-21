
<p align="center">
  <a href="" target="_blank">
  <!--TODO: update img src and href's below once our app is live and make sure that the links open in a new tab-->
    <img width="180" src="https://pinia.vuejs.org/logo.svg" alt="Colada logo">
  </a>
</p>
<br/>
<p align="center">
  <!--TODO: update img src and href's below once our app is live and make sure that the links open in a new tab-->
  <a href="https://opensource.org/licenses/MIT"><img src="https://badgen.net/badge/license/MIT/green" alt="license MIT"></a>
  <a href="https://npmjs.com/package/pinia"><img src="https://badgen.net/npm/v/pinia" alt="npm package"></a>
  <a href="https://chrome.google.com/webstore/category/extensions"><img src="https://badgen.net/chrome-web-store/v/ckkdlimhmcjmikdlpkmbgfkaikojcbjk" alt="chrome web store"></a>
  <a href="https://www.typescriptlang.org/docs/"><img src="https://badgen.net/badge/icon/typescript?icon=typescript&label" alt="typescript"></a>

</p>
<br/>

There are two ways to install the Colada Chrome extension:

## Install from the Chrome Web Store (Coming Soon!)
1. Navigate to [Colada on the Chrome Web Store](https://chrome.google.com/webstore/category/extensions), and click "Add to Chrome"

## Install from source

1.
```
cd colada-extension
npm install
npm run build
```
2. This will create a new `/dist` directory in `/colada-extension`
3. In Chrome, navigate to [chrome://extensions](chrome://extensions).
4. In the top right of the Extensions page, there is a toggle for "Developer Mode." Make sure this is toggled **ON**.
5. On the top left of the page, select "Load Unpacked", and select the `colada/colada-extension/dist` directory.

## *The perfect companion for [Pinia🍍](https://pinia.vuejs.org/ "Pinia homepage and documentation"), Vue's official state management library*
<br/>

## Colada offers a suite of tools for Vue developers working with the [Pinia state management library](https://pinia.vuejs.org/):
1. [Chrome DevTool Extension]()
2. [NPM package]() that serves as a [plugin](https://devtools.vuejs.org/plugin/plugins-guide.html) for the [Vue.js DevTools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=en)
3. [Pinia🍍](https://pinia.vuejs.org/) plugin to directly access and mutate your app's store

<br/>

## Core Features

- ✅  Minimal installation and automatic detection of Vue app
- 🔄  Direct integration into [Vue.js DevTools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=en), so developers can use Colada without needing to leave their existing devtool configuration
  - 🕰️  Time travel debugging
  - 🔎  Inspector panel for viewing your Vue app's Pinia state
- 💻  A [Chrome DevTool Extension]() providing enhanced features, including: 
  - 🕰️  Time travel debugging
  - 🔎  Inspector panel for viewing your Vue app's Pinia state

<br/>

## INSERT TIME TRAVEL DEBUGGING GIF HERE
<img width="800px" src="https://c.tenor.com/KEzW7ALwfUAAAAAM/cat-what.gif" alt="demo gif" />

<br/>
<br/>

# Getting Started

## Installation
0. Make sure you have the [Vue.js DevTools extension](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=en) installed
1. Install the [Colada npm Package]() in your app's root directory(?)
```bash
npm install colada-plugin --save-dev (can we do --save-dev yet?)
```

2. Add Colada to your Vue app
```js
// main.js

import { createApp } from 'vue';
import { createPinia } from 'pinia';
// import Colada Plugin
import Colada, { PiniaColadaPlugin } from 'colada-plugin';
import App from './App.vue';

const app = createApp(App);
const pinia = createPinia();

app.use(pinia);
pinia.use(PiniaColadaPlugin);
app.use(Colada);

app.mount('#app');
```

```js
// App.vue

// your Pinia stores
// MAKE SURE THAT THIS MATCHES THE 'id' of your stores
const store = useStore();
const counter = useCounterStore();

// **REQUIRED for Colada plugin use
window.store = {store, counter}
```

<br/>
<br/>

# How to Use Colada

## Using the Colada Vue DevTools Plugin
- Navigate to the Vue Devtools

### Time Travel Debugging
- Select the "Colada" timeline in the timeline view 
- **TURN OFF SCREENSHOTS <br/>
<img width="600px" src="https://mdswanson.com/static/chops-ux-step-4.png" alt="Time travel screenshot for plugin">
- Click on events automatically tracked on the timeline to travel through time and update your app's state

### Inspector Panel - View Your Apps State in Real Time!
- Select "Colada" in the component menu drop down
- Click on your Pinia store to view state, actions, and getters, updated in real time

## Using the Colada Chrome DevTool Extension




<br/>
<br/>

# How to Give Colada a Test Run With Our Demo App

1. Clone this repo
2. Navigate to the ```demo-project``` directory
```
cd demo-project
```
3. Install packages 
```bash
npm install #test comment for bash
npm install ../colada-plugin (we need to make sure our demo-project has colada as a dev dependency so we can just have the user do npm install)
npm run dev
```

<br/>
<br/>

# Contributing and Issues
Interested in conributing to Colada? Reach out to our core team
Feature requests or issues/bugs to report? Read our documentation on [feature requests]() and [issues/bugs]().

<br/>

# Release Notes
### Contributors
- Parker Steinberg • [LinkedIn](https://www.linkedin.com/in/parker-steinberg/) • [Github](https://github.com/parkersteinberg)
- Jonathan Chen • [LinkedIn](https://www.linkedin.com/in/jonathan-hp-chen/) • [Github](https://github.com/JonHPC)
- Vaughn Sulit • [LinkedIn](https://www.linkedin.com/in/bvaughnsulit/) • [Github](https://github.com/bvaughnsulit)
- Dan Steinbrook • [Github](https://github.com/dsteinbrook)

<br/>
0.14.0 | Initial release of Colada, more to come!


<br/>

# License
[MIT](http://opensource.org/licenses/MIT)