<script lang="ts" setup>
import { XCircleIcon } from '@heroicons/vue/24/outline';

const emit = defineEmits(['delete']);

const props = defineProps<{
  id: number;
  name: string;
  url: string;
  icon: string;
}>();

</script>

<template>
  <div 
    class="list-row flex items-center justify-between gap-4"
  >
    <a 
      :href="props.url"
      target="_blank"
      class="no-underline"
      rel="noopener noreferrer">
      <div class="flex items-center gap-2 flex-grow">
        <img :src="props.icon" alt="Bookmark Icon" class="bookmark-icon">
        <div>
          <h1 class="text-lg">{{ props.name }}</h1>
          <span class="text-xs">{{ props.url }}</span>
        </div>
      </div>
    </a>
    <div class="px-2" @click="() => emit('delete', props.id)">
      <XCircleIcon class="size-6 cursor-pointer"/>
    </div>
  </div>
</template>


<style>

</style>