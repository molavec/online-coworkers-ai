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
      <NuxtLink 
        v-for="ws in workspacesTitleExamples" 
        :key="ws" 
        to="/dashboard">
        <SpaceBubble :label="ws" />
      </NuxtLink>
    </div>
    <div class="p-16 w-full">
      <ul class="list bg-base-100 rounded-box shadow-md">
  
        <li class="p-4 pb-2 text-xs opacity-60 tracking-wide">More Spaces</li>
        
        <li class="list-row items-center">
          <!-- avatar -->
          <NuxtLink to="/dashboard">
            <div class="avatar avatar-placeholder">
              <div class="bg-red-500 text-neutral-content w-12 rounded-full">
                <span class="font-semibold">Go</span>
              </div>
            </div>
          </NuxtLink>
          <!-- Task -->
           <NuxtLink to="/dashboard">
             <div>
               <div class="text-lg font-semibold">Google Analytics Course</div>
             </div>
           </NuxtLink>
          <!-- button Ghost -->
          <NuxtLink to="/dashboard">
            <button class="btn btn-square btn-ghost">
              <svg class="size-[1.2em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g stroke-linejoin="round" stroke-linecap="round" stroke-width="2" fill="none" stroke="currentColor"><path d="M6 3L20 12 6 21 6 3z"/></g></svg>
            </button>
          </NuxtLink>
        </li>
        
      </ul>
    </div>
  </NuxtLayout>
</template>

<style scoped></style>
