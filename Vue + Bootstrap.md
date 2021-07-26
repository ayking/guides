- vue create [app name]
- npm install bootstrap bootstrap-vue
```
import Vue from 'vue'
import App from './App.vue'
import { BootstrapVue, IconsPlugin } from 'bootstrap-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

Vue.config.productionTip = false
// Make BootstrapVue available throughout your project

Vue.use(BootstrapVue)
// Optionally install the BootstrapVue icon components plugin
Vue.use(IconsPlugin)

new Vue({
  render: h => h(App),
}).$mount('#app')
```

Componment
```
<template>
  <div>
    <b-container class="bv-example-row">
      <b-row>
        <b-col>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import { BButton, BContainer, BRow, BCol } from "bootstrap-vue";

export default {
  name: "HelloWorld",
  created() {
  },
  components: {
    BButton,
    BContainer,
    BRow,
    BCol,
  },
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    test() {
    }
  },
};
</script>

```
