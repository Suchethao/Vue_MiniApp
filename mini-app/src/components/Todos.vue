<template>
  <div>
    <h2>Today's List</h2>
    <ul>
      <li v-for="(task, index) in filteredTasks" :key="index" :class="{ completed: task.completed }">
        <span>{{ task.text }}</span>
        <button @click="completeTask(index)">Complete</button>
      </li>
    </ul>
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
