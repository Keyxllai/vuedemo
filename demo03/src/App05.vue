<template>
  <!-- Class操作 -->
  <!--第一种 放置字符串 -->
  <div :class="Msg">放置字符串</div>
  <!--第二种 放置对象 -->
  <div :class="{seleted:isActive}">放置对象</div>
  <button @click="changeseleted">切换seleted</button>

  <!--第三种 放置数组 -->

  <div :class="arr">放置数组</div>
  <button @click="validateerror">校验操作样式数组</button>
</template> 

<script>
export default {
  name: "App",
  data() {
    return {
      Msg: "HelloWorld",
      isActive: true,
      arr: ['active', 'error']
    };
  },
  methods: {
    changeseleted: function(){
      this.isActive = !this.isActive;
    },
    validateerror: function(){
      this.arr.push('ErrorMsg')
    }
  },
};
</script>

<style scoped>
  .seleted{
    background: green;
  }
  .ErrorMsg{
    background: red;
  }
</style>