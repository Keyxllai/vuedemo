<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" />-->
  <HelloWorld msg="Hello Vue 3.0 + Vite" /> 
  <h1>{{Msg}}</h1>
  <h1 @click="ChangeMsg" v-once>{{Msg}}</h1>
  <input type="text" v-model="Msg" />
  <div>{{ htmlMsg }}</div>
  <div v-html="htmlMsg"></div>

  <div :class="sclass"></div>
  <div v-bind:class="sclass"></div>
</template> 

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      Msg : "Hello World",
      htmlMsg: "<h1>标题1</h1>",
      sclass: "cls1"
    }
  },
  methods: {
    ChangeMsg(){
      this.Msg = "qibao",
      this.sclass = "cls2"
    }
  },
}
</script>

<style scoped>
  .cls1{
    width: 100px;
    height: 100px;
    background: red;
  }

  .cls2{
    width: 100px;
    height: 100px;
    background: green;
  }
</style>
