<script setup lang="ts">
// No hay lógica específica aún
// Array bookmarks objects { id, name, url, icon }
const bookmarks = ref([
  { id: 1, name: 'Figma Project 1', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
  { id: 2, name: 'Figma Project 2', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
  { id: 3, name: 'Figma Project 3', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
])

</script>

<template>
  <NuxtLayout>
    <div class="bookmarks-view w-full">
      <h1 class="text-2xl font-light mb-8">Bookmarks</h1>
      <ul class="bookmark-list">
        <a v-for="bookmark in bookmarks" :key="bookmark.id" :href="bookmark.url" target="_blank" rel="noopener noreferrer">
          <li class="bookmark-item flex items-center gap-4 p-4 bg-gray-800 rounded-lg shadow-md mb-4">
            <img :src="bookmark.icon" alt="Bookmark Icon" class="bookmark-icon">
            <div>
              <h1 class="text-lg">{{ bookmark.name }}</h1>
              <span class="text-xs">{{ bookmark.url }}</span>
            </div> 
          </li>
        </a>
      </ul>
    </div>
  </NuxtLayout>
</template>

<style scoped></style>
