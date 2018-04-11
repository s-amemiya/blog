title: Preparation for using Vuex
date: 2018-04-11 00:00:00
tags: vue
---

# Add vuex

```shell
yarn add -D vuex
```

# Make ./store/index.js

```javascript
// ./store/index.js
import Vue from 'vue'
import Vuex from 'vuex'

Vue.use(Vuex)

const state = {}
const getters = {}
const actions = {}
const mutations = {}

export default new Vuex.Store({
  state,
  getters,
  actions,
  mutations
})

```

# Modify ./main.js

```javascript
// ./main.js
import Vue from 'vue'
import App from './App'
import router from './router'
import store from './store' // added

Vue.config.productionTip = false

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  store, // added
  components: { App },
  template: '<App/>'
})

```
