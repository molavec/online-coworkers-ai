<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps<{
  username: string
}>()

// Colores usados en los SpaceBubble del artboard MainView de Figma (completo)
const bubbleColors = [
  '#F53B57', // rojo principal
  '#FC7081', // rosa
  '#F7374F', // acento
  '#3A3838', // gris oscuro (texto)
  '#B2BC57', // verde lima
  '#CFBA00', // amarillo
  '#8FB264', // verde
  '#CA72BE', // violeta
]

const randomColor = ref(bubbleColors[Math.floor(Math.random() * bubbleColors.length)])
</script>

<template>
  <div class="tooltip tooltip-left flex flex-col items-center rounded-full shadow cursor-pointer">
    <div class="tooltip-content">
      <div class="rotate-5"> {{ username }} </div>
    </div>
    <div class="avatar avatar-placeholder">
      <div 
        class="bg-neutral text-neutral-content w-8 text-md rounded-full transition-discrete duration-300 ease-in-out"
        :style="{ background: randomColor }"
      >
        <span class="font-semibold">
          {{ props.username.charAt(0) }}{{ props.username.charAt(1) }}
        </span>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
