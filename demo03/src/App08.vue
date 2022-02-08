<template>
  <!--  v-if 重新渲染，性能差  -->
  <ol>
    <li v-for="(item,i) in news">{{item}} --> {{i}}</li>
  </ol>


  <ol>
    <li v-for="(item,i) in obj">{{item}} --> {{i}}</li>
  </ol>
</template> 

<script>
export default {
  name: "App",
  data() {
    return {
     news: [
       "news1",
       "news2"
     ],
     obj: {
       name:"seven",
       age: 2,
       tag: "child"
     }
    };
  }
};
</script>
