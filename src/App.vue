/* eslint-disable */

<template>
  <div id="app">
    <Loading v-show="loading" />
    <TodoList v-show="!loading" />
  </div>
</template>

<script>
import TodoList from "./components/TodoList";
import Loading from "./components/Loading";

export default {
  name: "App",
  components: {
    TodoList,
    Loading,
  },
  data() {
    return {
      loading: true,
    };
  },
  mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 3000);
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
