<script setup lang="ts">
import SpaceBubble from '~/components/SpaceBubble.vue'
</script>

<template>
  <div class="main-view">
    <h1>MainView</h1>
    <div class="spaces">
      <SpaceBubble label="Espacio 1" />
      <SpaceBubble label="Espacio 2" />
      <SpaceBubble label="Espacio 3" />
    </div>
    <section class="main-content">
      <h2>Bienvenido a tu espacio principal</h2>
      <p>Aquí puedes ver y gestionar tus espacios de trabajo, acceder a tus tareas y navegar entre vistas.</p>
      <NuxtLink to="/dashboard">Ir al Dashboard</NuxtLink>
      <NuxtLink to="/bookmarks">Ver Bookmarks</NuxtLink>
      <NuxtLink to="/tasks">Ver Tasks</NuxtLink>
    </section>
  </div>
</template>

<style scoped>
.main-view {
  padding: 2rem;
}
.spaces {
  display: flex;
  gap: 1rem;
  margin-bottom: 2rem;
}
.main-content {
  background: #f7f7f7;
  padding: 1.5rem;
  border-radius: 1rem;
}
</style>
