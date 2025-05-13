<script setup lang="ts">
// No hay lógica específica aún
</script>

<template>
  <div class="bookmarks-view">
    <h1>Bookmarks</h1>
    <ul class="bookmark-list">
      <li>
        <span>Bookmark 1</span>
        <NuxtLink to="/dashboard">Ir al Dashboard</NuxtLink>
      </li>
      <li>
        <span>Bookmark 2</span>
        <NuxtLink to="/tasks">Ir a Tasks</NuxtLink>
      </li>
      <li>
        <span>Bookmark 3</span>
        <NuxtLink to="/">Ir a Home</NuxtLink>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.bookmarks-view {
  padding: 2rem;
}
.bookmark-list {
  margin-top: 2rem;
  list-style: none;
  padding: 0;
}
.bookmark-list li {
  background: #f7f7f7;
  margin-bottom: 1rem;
  padding: 1rem;
  border-radius: 0.75rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
