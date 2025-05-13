<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  label: {
    type: String,
    required: true
  }
})

// Colores usados en los SpaceBubble del artboard MainView de Figma (completo)
const bubbleColors = [
  '#F53B57', // rojo principal
  '#FC7081', // rosa
  '#F7374F', // acento
  '#FEA3AD', // rosa claro
  '#3A3838', // gris oscuro (texto)
  '#FFF1F2', // fondo claro
  '#B2BC57', // verde lima
  '#CFBA00', // amarillo
  '#8FB264', // verde
  '#B2C6D5', // azul grisáceo
  '#CA72BE', // violeta
]

const randomColor = ref(bubbleColors[Math.floor(Math.random() * bubbleColors.length)])
</script>

<template>
  <div class="space-bubble flex flex-col items-center gap-2 px-6 py-3 rounded-full shadow">
    <div class="avatar placeholder">
      <div 
        class="rounded-full flex items-center justify-center"
        :style="{ background: randomColor, width: '72px', height: '72px' }"
      >
        <span class="text-3xl font-extrabold uppercase text-white drop-shadow">
          {{ props.label.charAt(0) }}{{ props.label.charAt(1) }}
        </span>
      </div>
    </div>
    <span class="font-semibold text-lg mt-1">{{ props.label }}</span>
  </div>
</template>

<style scoped>
.space-bubble {
  transition: background 0.3s;
}
</style>
