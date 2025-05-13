<script setup lang="ts">
// Motivational phrases array
const motivationalPhrases = [
  "¡Bienvenido a tu espacio de trabajo!",
  "¡Aquí comienza tu jornada productiva!",
  "¡Listo para conquistar el día!",
  "¡Cada tarea es un paso hacia el éxito!",
  "¡Tu espacio, tus reglas!",
]
const randomPhrase = motivationalPhrases[Math.floor(Math.random() * motivationalPhrases.length)]
// const { t } = useI18n()

// Workspaces title examples array
const workspacesTitleExamples = [
  "Marketing Meta",
  "Woocommerce",
  "Tesis",
  "Ocio",
  "New",
]

</script>

<template>
  <NuxtLayout name="main">
    <h1 class="text-3xl font-bold mb-4">{{randomPhrase}}</h1>
    <div class="flex flex-wrap gap-2 justify-center items-center min-h-[25vh]">
      <SpaceBubble 
        v-for="ws in workspacesTitleExamples" 
        :key="ws" 
        :label="ws" />
    </div>
    <div class="p-16 w-full">
      <ul class="list bg-base-100 rounded-box shadow-md">
  
        <li class="p-4 pb-2 text-xs opacity-60 tracking-wide">More Spaces</li>
        
        <li class="list-row">
          <div><img class="size-10 rounded-box" src="https://img.daisyui.com/images/profile/demo/1@94.webp"/></div>
          <div>
            <div>Dio Lupa</div>
            <div class="text-xs uppercase font-semibold opacity-60">Remaining Reason</div>
          </div>
          <button class="btn btn-square btn-ghost">
            <svg class="size-[1.2em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g stroke-linejoin="round" stroke-linecap="round" stroke-width="2" fill="none" stroke="currentColor"><path d="M6 3L20 12 6 21 6 3z"></path></g></svg>
          </button>
          <button class="btn btn-square btn-ghost">
            <svg class="size-[1.2em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g stroke-linejoin="round" stroke-linecap="round" stroke-width="2" fill="none" stroke="currentColor"><path d="M19 14c1.49-1.46 3-3.21 3-5.5A5.5 5.5 0 0 0 16.5 3c-1.76 0-3 .5-4.5 2-1.5-1.5-2.74-2-4.5-2A5.5 5.5 0 0 0 2 8.5c0 2.3 1.5 4.05 3 5.5l7 7Z"></path></g></svg>
          </button>
        </li>
        
        <li class="list-row">
          <div><img class="size-10 rounded-box" src="https://img.daisyui.com/images/profile/demo/4@94.webp"/></div>
          <div>
            <div>Ellie Beilish</div>
            <div class="text-xs uppercase font-semibold opacity-60">Bears of a fever</div>
          </div>
          <button class="btn btn-square btn-ghost">
            <svg class="size-[1.2em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g stroke-linejoin="round" stroke-linecap="round" stroke-width="2" fill="none" stroke="currentColor"><path d="M6 3L20 12 6 21 6 3z"></path></g></svg>
          </button>
          <button class="btn btn-square btn-ghost">
            <svg class="size-[1.2em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g stroke-linejoin="round" stroke-linecap="round" stroke-width="2" fill="none" stroke="currentColor"><path d="M19 14c1.49-1.46 3-3.21 3-5.5A5.5 5.5 0 0 0 16.5 3c-1.76 0-3 .5-4.5 2-1.5-1.5-2.74-2-4.5-2A5.5 5.5 0 0 0 2 8.5c0 2.3 1.5 4.05 3 5.5l7 7Z"></path></g></svg>
          </button>
        </li>
        
        <li class="list-row">
          <div><img class="size-10 rounded-box" src="https://img.daisyui.com/images/profile/demo/3@94.webp"/></div>
          <div>
            <div>Sabrino Gardener</div>
            <div class="text-xs uppercase font-semibold opacity-60">Cappuccino</div>
          </div>
          <button class="btn btn-square btn-ghost">
            <svg class="size-[1.2em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g stroke-linejoin="round" stroke-linecap="round" stroke-width="2" fill="none" stroke="currentColor"><path d="M6 3L20 12 6 21 6 3z"></path></g></svg>
          </button>
          <button class="btn btn-square btn-ghost">
            <svg class="size-[1.2em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g stroke-linejoin="round" stroke-linecap="round" stroke-width="2" fill="none" stroke="currentColor"><path d="M19 14c1.49-1.46 3-3.21 3-5.5A5.5 5.5 0 0 0 16.5 3c-1.76 0-3 .5-4.5 2-1.5-1.5-2.74-2-4.5-2A5.5 5.5 0 0 0 2 8.5c0 2.3 1.5 4.05 3 5.5l7 7Z"></path></g></svg>
          </button>
        </li>
        
      </ul>
    </div>
  </NuxtLayout>
</template>

<style scoped></style>
