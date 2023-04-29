<template>
  <div>
    <!-- Display the heading of the list -->
    <h2>Today's List</h2>
    
    <!-- Display the list of tasks if there are any -->
    <ul v-if="filteredTasks.length > 0">
      <li v-for="(task, index) in filteredTasks" :key="index" :class="{ completed: task.completed }">
        <span>{{ task.text }}</span>
        <button @click="completeTask(index)">Complete</button>
      </li>
    </ul>
    
    <!-- Display a message if there are no tasks in the list -->
    <p v-else> Add a task to your CheckMate list to get started. </p>
    
    <!-- Form to add new tasks to the list -->
    <form @submit.prevent="addTask">
      <label for="newTask">Add new task:</label>
      <input type="text" id="newTask" v-model="newTaskText">
      <button type="submit">Add</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "AppTodos",
  
  // Set up the initial data of the component
  data() {
    return {
      tasks: [
        { text: "Learn Vue.js", completed: false },
        { text: "Build a project", completed: false },
        { text: "Deploy to production", completed: false },
      ],
      newTaskText: "",
    };
  },
  
  // Define the methods used in the component
  methods: {
    addTask() {
      if (this.newTaskText.trim() !== "") {
        this.tasks.push({ text: this.newTaskText, completed: false });
        this.newTaskText = "";
      }
    },
    completeTask(index) {
      this.tasks[index].completed = true;
    },
  },
  
  // Compute the list of tasks that still need to be completed
  computed: {
    filteredTasks() {
      return this.tasks.filter((task) => !task.completed);
    },
  },
};
</script>

<style scoped>
.completed {
  text-decoration: line-through;
}
</style>
