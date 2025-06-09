<script setup lang="ts">
import {XCircleIcon} from '@heroicons/vue/24/outline'
// Array bookmarks objects { id, name, url, icon }
const bookmarks = ref([
  { id: 1, name: 'Figma Project 1', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
  { id: 2, name: 'Figma Project 2', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
  { id: 3, name: 'Figma Project 3', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
])

</script>

<template>
  <div>

    <div class="w-full p-2">
      <!-- title -->
      <h1 class="text-2xl font-light mb-4">Bookmarks</h1>

      <!-- content -->
      <ul class="list rounded-box shadow bg-gray-800">
        <li 
          v-for="bookmark in bookmarks" 
          :key="bookmark.id" 
          class="list-row flex items-center justify-between gap-4"
        >
          <a 
            :href="bookmark.url"
            target="_blank"
            class="no-underline"
            rel="noopener noreferrer">
            <div class="flex items-center gap-2 flex-grow">
              <img :src="bookmark.icon" alt="Bookmark Icon" class="bookmark-icon">
              <div>
                <h1 class="text-lg">{{ bookmark.name }}</h1>
                <span class="text-xs">{{ bookmark.url }}</span>
              </div>
            </div>
          </a>
          <div class="px-2" @click.stop="bookmarks.splice(bookmarks.indexOf(bookmark), 1)">
            <XCircleIcon class="size-6 cursor-pointer"/>
          </div>
        </li>
      </ul>
    </div>

  </div>
</template>

<style scoped></style>
