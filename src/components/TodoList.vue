<template>
  <ul>
    <li v-for="(task, i) in tasks" :key="i">
      {{ task }}
      <button @click="deleteTaks(i)">Eliminar</button>
    </li>
  </ul>
</template>

<script>
export default {
  name: "TodoList",
  props: {
    tasks: [],
    deleteTaks: { type: Function },
  },
};
</script>

<style>
</style>