<template>
  <!-- Class操作 -->
  <!--第一种 放置字符串 -->
  <div :style="Msg">放置字符串</div>
  <!--第二种 放置对象 -->
  <div :style="{background:'purple'}">放置对象</div>
  <div :style="styleObj">放置对象</div>
  <button @click="changeseleted">切换seleted</button>

  <!--第三种 放置数组对象 -->

  <div :style="[styleObj,{width:'500px'}]">放置数组+对象</div>
</template> 

<script>
export default {
  name: "App",
  data() {
    return {
      Msg: "background:yellow",
      styleObj:{
        'background-color': 'green',
        border: '1px solid blue'
      }
    };
  },
  methods: {
    changeseleted: function(){
      this.styleObj['background-color'] = 'pink';
    }
  },
};
</script>

<style scoped>
  .seleted{
    background: yellowgreen;
  }
  .ErrorMsg{
    background: red;
  }
</style>