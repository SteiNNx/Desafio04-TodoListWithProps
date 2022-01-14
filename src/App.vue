<template>
  <div id="app">
    <section>
      <label for="txt_task">Tarea</label>
      <input
        id="txt_task"
        type="text"
        v-model="task"
        placeholder="ingrese nueva tarea"
      />
      <button @click="addTask">Agregar</button>
    </section>
    <section>
      <TodoList :tasks="tasks" :deleteTaks="deleteTaks" />
    </section>
  </div>
</template>

<script>
import TodoList from "@/components/TodoList.vue";

export default {
  name: "App",
  components: {
    TodoList,
  },
  data() {
    return {
      task: "",
      tasks: [],
    };
  },
  methods: {
    addTask() {
      const { task } = this;
      this.tasks.push(task);
    },
    deleteTaks(indexTask) {
      this.tasks.splice(indexTask, 1);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

label {
  font-weight: 700;
  margin: 0rem 1rem;
}

button {
  padding: 0.1rem 0.75rem;
  margin: 0rem 1rem;
}
</style>
