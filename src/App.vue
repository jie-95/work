<template>
  <div id="app">
    <HelloWorld :total="total" />
    <Index
      :total="total"
      :currentPage="currentPage"
      :pageSize="10"
      @pageChange="pageChangehh"
    />
  </div>
</template>
<script>
/* eslint-disable */
import HelloWorld from "./components/MyIndex.vue";
import Index from "./components/TeacherIndex.vue";
export default {
  // eslint-disable-next-line
  data() {
    return {
      total: 80,
      currentPage: 1,
    };
  },
  components: {
    HelloWorld,
    Index,
  },
  methods: {
    pageChangehh(val) {
      this.currentPage = val;
    },
  },
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
