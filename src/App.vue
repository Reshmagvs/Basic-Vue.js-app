<template>
  <div>
    <h1>Vue Task List App</h1>
    <TaskList />
  </div>
</template>

<script>
import TaskList from "./components/TaskList.vue";

export default {
  components: {
    TaskList,
  },
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  text-align: center;
}
</style>

