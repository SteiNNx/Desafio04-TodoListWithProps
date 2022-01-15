<template>
  <ul>
    <li v-for="(task, i) in tasks" :key="i">
      {{ task }}
      <button @click="emitedDeleteTask(i)">Eliminar</button>
    </li>
  </ul>
</template>

<script>
export default {
  name: "TodoList",
  props: {
    tasks: [],
  },
  methods: {
    emitedDeleteTask(index) {
      this.$emit("deleteTaks", index);
    },
  },
};
</script>

<style scoped>
ul {
  font-weight: 700;
}
</style>