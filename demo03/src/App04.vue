<template>
  <!-- 计算属性 -->
  <h1>{{ Msg.split("").reverse().join("") }}</h1>
  <h1>{{ reverseMsg }}</h1>

  <!-- watch监听数据变化 -->

  <input type="text" v-model="Msg" />
  <h2>{{ Msg }}</h2>
</template> 

<script>
export default {
  name: "App",
  data() {
    return {
      Msg: "HelloWorld",
    };
  },
  computed: {
    reverseMsg: function () {
      return this.Msg.split("").reverse().join("");
    },
  },
  methods: {
    changeName() {
      this.attrName = "id";
    },
  },
  watch: {
    Msg: function (newValue, oldValue) {
      if (newValue.length < 10) {
        alert("输入值长度小于10");
      }
    },
  },
};
</script>