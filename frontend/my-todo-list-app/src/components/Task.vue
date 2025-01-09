<template>
  <div class="task-container">
    <h2>{{ task.title }}</h2>
    <img :src="task.image" :alt="task.title" />
    <p>{{ task.description }}</p>
  </div>
</template>

<script>
export default {
  name: "TaskItems",
  props: {
    task: Object,
  },
};
</script>

<style scoped>
.task-container {
  border: 1px solid #e6e3d2;
  border-radius: 8px;
  padding: 15px;
  margin: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: box-shadow 0.3s ease;
}
.task-container:hover {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}
.task-container img {
  max-width: 100%;
  height: auto;
  border-radius: 4px;
}
.task-container h2 {
  font-size: 1.5em;
  margin-bottom: 8px;
}
.task-container p {
  font-size: 1em;
  color: #555;
}
</style>
