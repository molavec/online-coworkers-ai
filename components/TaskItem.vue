<script lang="ts" setup>
import { XCircleIcon } from '@heroicons/vue/24/outline';

const props = defineProps<{
  id: number;
  title: string;
  description: string;
}>();

const model = defineModel<boolean>()
const emit = defineEmits(['delete']);

</script>
<template>
  <div 
    class="list-row flex items-center justify-between gap-4"
  >
    <div class="flex items-center gap-4 flex-grow">
      <input v-model="model" type="checkbox" class="checkbox" >
      <div>
        <h1 class="text-lg">{{ props.title }}</h1>
        <span class="text-xs">{{ props.description }}</span>
      </div>
    </div>
    <div class="px-2" @delete="() => emit('delete', props.id)">
      <XCircleIcon class="size-6 cursor-pointer"/>
    </div>
  </div>
</template>


<style>

</style>