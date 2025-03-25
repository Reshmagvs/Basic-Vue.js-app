<template>
    <div>
      <h2>Task List</h2>
      <input v-model="newTask" placeholder="Enter a task" />
      <button @click="addTask">Add Task</button>
  
      <ul>
        <li v-for="(task, index) in tasks" :key="index">
          {{ task }}
          <button @click="removeTask(index)">Remove</button>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newTask: "",
        tasks: [],
      };
    },
    methods: {
      addTask() {
        if (this.newTask.trim()) {
          this.tasks.push(this.newTask);
          this.newTask = "";
        }
      },
      removeTask(index) {
        this.tasks.splice(index, 1);
      },
    },
  };
  </script>
  
  <style scoped>
  button {
    margin-left: 10px;
    cursor: pointer;
  }
  </style>
  