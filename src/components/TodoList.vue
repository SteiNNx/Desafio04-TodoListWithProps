<template>
  <ul>
    <li v-for="(task, i) in tasks" :key="i">
      {{ task }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "TodoList",
  props: {
    tasks: [],
  },
};
</script>

<style>
</style>