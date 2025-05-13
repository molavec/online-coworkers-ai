<script setup lang="ts">
// No hay lógica específica aún
</script>

<template>
  <div class="dashboard-view">
    <h1>Dashboard</h1>
    <div class="widgets">
      <div class="widget">
        <h2>Resumen</h2>
        <p>Visualiza el estado general de tus espacios y tareas.</p>
      </div>
      <div class="widget">
        <h2>Actividad Reciente</h2>
        <ul>
          <li>Espacio 1 actualizado</li>
          <li>Nueva tarea agregada</li>
          <li>Bookmark guardado</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.dashboard-view {
  padding: 2rem;
}
.widgets {
  display: flex;
  gap: 2rem;
  margin-top: 2rem;
}
.widget {
  background: #f7f7f7;
  padding: 1.5rem;
  border-radius: 1rem;
  flex: 1;
}
</style>
