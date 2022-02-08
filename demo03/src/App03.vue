<template>
  <!-- 动态指令-->
  <div v-bind:[attrName] = "color"></div>
  <div :[attrName] = "color"></div>

  <button @click="changeName">切换颜色</button>
  <button @[eventName]="changeName">切换颜色</button>
</template> 

<script>

export default {
  name: 'App',
  data() {
    return {
      attrName : "class",
      color: "block",
      eventName: "click"
    }
  },
  methods: {
    changeName(){
      this.attrName = "id"
    }
  },
}
</script>

<style>
  #block {
    width: 100px;
    height: 100px;
    background: green;
  }

  .block {
    width: 100px;
    height: 100px;
    background: red;
  }
</style>