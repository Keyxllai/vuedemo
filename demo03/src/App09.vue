<template>
  <!--  事件  -->
  <h1 @click="click1">点击事件{{num}}</h1>
  <h1 @click="num+=2">点击事件{{num}}</h1>

  <h1 @click="add10(10)">点击事件{{num}}</h1>

  <h1 @click="addar10(20, $event)">点击事件{{num}}</h1>


  <h1 :style="{background: color}" @click="addar10(20, $event),changeColor()">点击事件{{num}}</h1>

  <h1 @click.once="addar10(20, $event)">事件修饰符{{num}}</h1>
</template> 

<script>
export default {
  name: "App",
  data() {
    return {
      num: 0,
      color:'red'
    };
  },
  methods: {
    click1: function () {
      this.num += 2;
    },
    add10: function (number) {
      this.num += number;
    },
    addar10: function (number, event) {
      console.log(event);
      this.num += number;
    },
    changeColor: function(){
      this.color = 'purple'
    }
  },
};
</script>
