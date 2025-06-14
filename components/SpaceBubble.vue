<script setup lang="ts">
import { ref, onMounted } from 'vue'

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

const randomColor = ref('#F53B57') // Default color

onMounted(() => {
  randomColor.value = bubbleColors[Math.floor(Math.random() * bubbleColors.length)]
})
</script>

<template>
  <div class="space-bubble flex flex-col items-center gap-2 p-3 rounded-full shadow">
    <div class="avatar avatar-placeholder">
      <div 
        class="bg-neutral text-neutral-content text-3xl hover:text-4xl  w-24 hover:w-32 rounded-full transition-discrete duration-300 ease-in-out"
        :style="{ background: randomColor }"
      >
        <span class="font-semibold">
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