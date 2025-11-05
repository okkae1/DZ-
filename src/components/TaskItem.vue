<template>
  <div class="task-card">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<script setup lang="ts">
interface Task {
  id: string;
  title: string;
  text: string;
}

defineProps<{
  task: Task;
}>();
</script>

<style scoped>
.task-card {
  border: 1px solid #ccc;
  padding: 12px;
  margin-bottom: 8px;
  border-radius: 8px;
  background-color: #f9f9f9;
}
</style>
