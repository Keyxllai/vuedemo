<template>
  <!--  v-if 重新渲染，性能差  -->
  <div v-if="user.role == 'VIP'">VIP</div>
  <div v-else-if="user.role == '超级VIP'">超级VIP</div>

  <div v-else>User</div>

  <button @click="changeuser">VIP过期</button>


  <!--  DOM树存在 display设置位none   -->
  <h1 v-show="isShow">显示内容</h1>
   <button @click="toggleShow">toggle</button>
</template> 

<script>
export default {
  name: "App",
  data() {
    return {
      user: {
        role: "VIP",
        name: "seven",
      },
      isShow: true
    };
  },
  methods: {
    changeuser: function () {
      this.user.role = "user";
    },
    toggleShow: function(){
      this.isShow = !this.isShow  
    }
  },
};
</script>
