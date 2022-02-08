<template>
  <!-- 模板语法使用js表达式-->
  <h1>{{Msg}}</h1>
  <h1>{{Msg.split('').reverse().join('')}}</h1>

  <h1>{{color =='green' ? "开心" : "难过"}}</h1>

</template> 

<script>

export default {
  name: 'App',
  data() {
    return {
      Msg : "Hello World",
      color: "green"
    }
  }
}
</script>
