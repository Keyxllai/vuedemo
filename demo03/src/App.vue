<template>
  <div>
    <!--  双向绑定  -->
    <input v-model="searchKey" type="text" @click="searchKeyEvent()" />
    <h1>{{ searchKey }}</h1>

    <textarea v-model="keys" name="fd" id="" cols="30" rows="10"></textarea>
    <h1>{{ keys }}</h1>

    <input v-model="checked" type="checkbox" name="like" id="" value="内容" />
    <h1>{{ checked }}</h1>
    <input
      v-model="checked1"
      type="checkbox"
      name="like"
      id=""
      true-value="X"
      false-value="U"
    />
    <h1>{{ checked1 }}</h1>

    <!--  复选  -->
    <input v-model="values" type="checkbox" name="likes" id="" value="1" />
    <input v-model="values" type="checkbox" name="likes" id="" value="2" />
    <input v-model="values" type="checkbox" name="likes" id="" value="3" />
    <h1>{{ values }}</h1>

    <!--  单选  -->
    <input type="radio" v-model="selected" name="sex" id="" value="man" />
    <input type="radio" v-model="selected" name="sex" id="" value="women" />
    <h1>{{ selected }}</h1>

    <select name="city" v-model="city" id="">
      <option value="成都">成都</option>
      <option value="重庆">重庆</option>
      <option value="西安">西安</option>
    </select>
    <h1>{{ city }}</h1>

    <h1>{{ searchKey }}</h1>

    <input v-model.lazy="searchKey" type="text" @click="searchKeyEvent()" />
    <h1>{{ searchKey }}</h1>

    <input
      v-model.lazy.number="searchKey"
      type="text"
      @click="searchKeyEvent()"
    />
    <h1>{{ searchKey }}</h1>

    <input v-model.trim="searchKey" type="text" @click="searchKeyEvent()" />
    <h1>{{ searchKey }}</h1>
  </div>
</template> 

<script>
Event;
export default {
  name: "App",
  data() {
    return {
      searchKey: "百度一下",
      keys: "",
      checked: false,
      values: [],
      selected: "",
      city: "",
      checked1: "",
    };
  },
  methods: {
    searchKeyEvent: function () {
      console.log("执行search操作");
    },
  },
};
</script>
