<script setup lang="ts">
import { ChevronRightIcon, ChevronLeftIcon } from '@heroicons/vue/24/outline';


const isSidebarCollapsed = ref(false)
const toggleSidebar = () => {
  isSidebarCollapsed.value = !isSidebarCollapsed.value
}

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
  <div>
    <!-- header -->
    <div class="flex items-center justify-between bg-queonda-500 p-2">
      <div class="left">
        <NuxtLink to="/">
          <WorkspacesLogo />
        </NuxtLink>
      </div>
      <div class="right flex items-center gap-2">
        <select class="select">
          <option disabled selected>Pick a color</option>
          <option v-for="ws in workspacesTitleExamples" :key="ws">{{ws}}</option>
        </select>
        <!-- dark/ligth theme -->
        <ClientOnly >
          <SwitchTheme />
        </ClientOnly>
        <div class="avatar avatar-placeholder">
          <div class="bg-neutral text-neutral-content w-10 rounded-full">
            <span>SY</span>
          </div>
        </div>
      </div>
    </div>

    <!-- content -->
    <div class="flex gap-2 min-h-96 p-2">
      <!-- sidebar -->
      <div 
        class="flex flex-col gap-2 p-2 min-h-full transition-discrete duration-300 ease-in-out"
        :class="isSidebarCollapsed ? 'w-12' : 'w-42'"
      >
        <NuxtLink to="/dashboard" class="rounded-2xl p-2 bg-gray-800 shadow-xs shadow-red-600">
          {{ isSidebarCollapsed ? 'D' : 'Dashboard' }}
        </NuxtLink>
        <NuxtLink to="/bookmarks" class="rounded-2xl p-2">
          {{ isSidebarCollapsed ? 'B' : 'Bookmarks' }}
        </NuxtLink>
        <NuxtLink to="/tasks" class="rounded-2xl p-2">
          {{ isSidebarCollapsed ? 'T' : 'Tasks' }}
        </NuxtLink>
      </div>
      <!-- divider bar -->
      <div class="flex flex-col items-center">
        <div class="border-r-2 min-h-6" />
        <div class="rounded-full border-2 p-1">
          <ChevronRightIcon
            v-if="isSidebarCollapsed"
            class="size-4 cursor-pointer"
            @click="toggleSidebar"
            />
          <ChevronLeftIcon
            v-else
            class="size-4 cursor-pointer"
            @click="toggleSidebar"
          />
          <!-- <div class='font-bold' @click="toggleSidebar">{{ isSidebarCollapsed ? '>' : '<' }}</div> -->
        </div>
        <div class="border-r-2 min-h-full" />
      </div>
      <!-- main content -->
      <slot />
    </div>

  </div>
</template>