<script setup>
import { ref } from "vue"

//compositions api
const name = ref("mir kamrul ahsan asif")
const status = ref("active")
const tasks = ref(["task-1 composition api", "task-2", "task-3"])
const newTask = ref("")

const changeStatusToActive = () => {
  status.value = "active"
}
const changeStatusToInactive = () => {
  status.value = "inactive"
}
const changeStatusToPending = () => {
  status.value = "pending"
}

function addTask() {
  if (newTask.value.trim() !== "") {
    tasks.value.push(newTask.value)
    newTask.value = ""
  }
}

function deleteTask(index) {
  tasks.value.splice(index, 1)
}

// return {
//   name,
//   status,
//   tasks,
//   changeStatusToActive,
//   changeStatusToInactive,
//   changeStatusToPending,
// }

//options api
/* export default {
  data() {
    return {
      message: "hello vue",
      name: "Jon Jones",
      status: "",
      tasks: ["task-1", "task-2", "task-3"],
      link: "https://google.com/",
    }
  },
  methods: {
    changeStatusToActive() {
      this.status = "active"
    },
    changeStatusToInactive() {
      this.status = "inactive"
    },
    changeStatusToPending() {
      this.status = "pending"
    },
  },
} */
</script>

<template>
  <h2 class="bg-slate-700 p-16 text-white text-3xl text-center">to do app</h2>
  <div class="bg-gray-300 p-10">
    <h1>{{ message }}</h1>
    <h1>
      {{ name }}
      <span v-if="status === 'active'">is active</span>
      <span v-else-if="status === 'inactive'">is inactive</span>
      <span v-else-if="status === 'pending'">pending...</span>
      <span v-else>status not found</span>
    </h1>
    <h2>Tasks</h2>
    <form @submit.prevent="addTask">
      <label for="newTask">New Task</label>
      <input type="text" id="newTask" name="newTask" v-model="newTask" />
      <input type="submit" value="Add Task" />
    </form>
    <ul>
      <li v-for="(task, index) in tasks" :key="task">
        <span>{{ task }}</span>
        <button @click="deleteTask(index)">delete</button>
      </li>
    </ul>
    <a :href="link">visit google</a>
    <br />
    <!-- <button v-on:click="changeStatusToActive">active</button> -->
    <button @click="changeStatusToActive">active</button>
    <button @click="changeStatusToInactive">inactive</button>
    <button @click="changeStatusToPending">pending</button>
    <br />
    <br />
  </div>
</template>

<style scoped>
span {
  color: blueviolet;
}
</style>
