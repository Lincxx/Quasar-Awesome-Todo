<template>
  <q-page padding>
    <ul>
      <li v-for="(task, index) in tasks" :key="index">
        <div>{{ task.name }}</div>
        <small>{{ task.dueDate }} @ {{ task.dueTime }}</small>
        <button @click="deleteTask(index)">X</button>
      </li>
    </ul>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      tasks: [
        {
          name: "Go to shop",
          dueDate: "5/12/2019",
          dueTime: "18:34"
        },
        {
          name: "Get Bananas",
          dueDate: "5/15/2019",
          dueTime: "1:45"
        },
        {
          name: "Get appples",
          dueDate: "6/1/2019",
          dueTime: "8:34"
        }
      ]
    };
  },
  methods: {
    deleteTask(index) {
      this.tasks.splice(index, 1);
    }
  }
};
</script>

<style>
</style>
