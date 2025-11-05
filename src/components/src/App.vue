<template>
  <div>
    <h1>Список дел</h1>
    <div v-for="task in tasks" :key="task.id">
      <TaskItem :task="task" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import TaskItem from './components/TaskItem.vue';

interface Task {
  id: string;
  title: string;
  text: string;
}

const tasks = ref<Task[]>([
  {
    id: '1',
    title: 'Купить продукты',
    text: 'Молоко, яйца, хлеб, овощи'
  },
  {
    id: '2',
    title: 'Созвон с командой',
    text: 'Обсудить задачи на неделю в 15:00'
  },
  {
    id: '3',
    title: 'Написать отчет',
    text: 'Подготовить отчет по проекту до конца дня'
  }
]);
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  padding: 20px;
  max-width: 600px;
  margin: 0 auto;
}
</style>
