<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="search-box">
    <input
      v-model="searchQuery"
      @input="handleInput"
      type="text"
      placeholder="搜索"
    />
  </div>

  <div class="recommend">
    <More></More>
  </div>
</template>

<script>
import More from './components/More.vue'

// export default {
//   name: 'App',
//   components: {
//     // HelloWorld
//   }
// }
export default {
  name: 'App',
  components: {
      More
   },
  data() {
    return {
      searchQuery: "",
    };
  },
  methods: {
    handleInput() {
      // 在这里可以添加实时搜索的逻辑
    },
    handleSearch() {
      // 在这里可以添加搜索按钮点击后的逻辑
      alert("搜索：" + this.searchQuery);
    },
  },
};
</script>

<style>
.search-box {
  display: flex;
  align-items: center;
}

input {
  flex: 1;
  padding: 8px;
  font-size: 15px;
  border: 1px solid #ccc;
  border-radius: 15px 15px 15px 15px;
  outline: none;
  text-align: center;
}

</style>
