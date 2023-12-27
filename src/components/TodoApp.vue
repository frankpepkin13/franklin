<template>
    <div class="max-w-md mx-auto p-4 bg-gray-100 rounded-md shadow-md">
      <h1 class="text-3xl font-bold mb-4 text-gray-800 text-center">Todo App</h1>
      <div class="mb-4">
        <input type="text" v-model="newTask" @keyup.enter="addTask"
          class="w-full p-3 border border-gray-300 rounded-md placeholder-gray-500 focus:outline-none" 
          placeholder="Add a new task..." />
      </div>
      <ul>
        <li v-for="(task, index) in tasks" :key="index" 
          class="flex items-center justify-between border-b py-3">
          <div class="flex items-center">
            <input type="checkbox" @change="toggleComplete(index)" :checked="task.completed" 
              class="mr-3 h-5 w-5 rounded border-gray-400 focus:outline-none focus:ring focus:border-blue-400" />
            <span :class="{ 'line-through': task.completed }" class="text-lg text-gray-800">{{ task.name }}</span>
          </div>
          <div>
            <button @click="deleteTask(index)" class="px-3 text-gray-600 hover:text-red-600 focus:outline-none">Delete</button>
          </div>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newTask: '',
        tasks: []
      };
    },
    methods: {
      addTask() {
        if (this.newTask.trim() !== '') {
          this.tasks.push({ name: this.newTask, completed: false });
          this.newTask = '';
        }
      },
      deleteTask(index) {
        this.tasks.splice(index, 1);
      },
      toggleComplete(index) {
        this.tasks[index].completed = !this.tasks[index].completed;
      }
    }
  };
  </script>
  
  <style scoped>
  
  .line-through {
    text-decoration: line-through;
  }
  </style>
  