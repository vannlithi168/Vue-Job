<script setup>
import { ref, onMounted } from "vue";

const name = ref("test");
const status = ref("active");
const tasks = ref(["task1", "task2", "task3"]);
const newTask = "";

const link = ref("https://google");

const toggleStatus = () => {
  if (status.value === "active") {
    status.value = "inactive";
  } else if (status.value === "pending") {
    status.value = "active";
  } else {
    status.value = "pending";
  }
};

const addTask = () => {
  if (newTask.value.trim() !== "") {
    tasks.value.push(newTask.value);
    newTask.value = "";
  }
};

const deleteTask = (index) => {
  tasks.value.splice(index, 1);
};

onMounted(async () => {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/todos");
    const data = await response.json();
    tasks.value = data.map((task) => task.title);
  } catch (error) {
    console.log("error fetching task");
  }
});
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <form @submit.prevent="addTask">
    <label for="newTask">Add task: </label>
    <input type="text" id="newTask" name="newTask" v-model="newTask" />
    <button type="submit">Submit</button>
  </form>

  <ul>
    <li v-for="(task, index) in tasks" :key="task">
      <span>{{ task }} </span>
      <button @click="deleteTask(index)">Delete</button>
    </li>
  </ul>
  <!-- <a v-bind:href="link">Redirect to Google || </a>
  <a :href="link" :style="'background-color: red; padding: 10px;'">Google</a> -->

  <button @click="toggleStatus">Change Status</button>
</template>

<style scoped></style>
