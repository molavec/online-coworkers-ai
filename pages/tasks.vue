<script setup lang="ts">
// No hay lógica específica aún
</script>

<template>
  <div class="tasks-view">
    <h1>TasksView</h1>
    <ul class="task-list">
      <li>
        <input id="task1" type="checkbox">
        <label for="task1">Tarea 1: Diseñar wireframe</label>
      </li>
      <li>
        <input id="task2" type="checkbox">
        <label for="task2">Tarea 2: Revisar dashboard</label>
      </li>
      <li>
        <input id="task3" type="checkbox">
        <label for="task3">Tarea 3: Añadir bookmark</label>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.tasks-view {
  padding: 2rem;
}
.task-list {
  margin-top: 2rem;
  list-style: none;
  padding: 0;
}
.task-list li {
  background: #f7f7f7;
  margin-bottom: 1rem;
  padding: 1rem;
  border-radius: 0.75rem;
  display: flex;
  align-items: center;
  gap: 1rem;
}
</style>
