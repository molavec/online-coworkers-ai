<script setup lang="ts">
import WorkspacesLogo from '~/components/WorkspacesLogo.vue'
</script>
<template>
  <div>
    <!-- header -->
    <div class="flex items-center justify-between p-2">
      <div class="left">
        <NuxtLink to="/">
          <WorkspacesLogo />
        </NuxtLink>
      </div>
      <div class="right flex items-center gap-2">
        <SwitchTheme />
        <div class="avatar avatar-placeholder">
          <div class="bg-neutral text-neutral-content w-12 rounded-full">
            <span>SY</span>
          </div>
        </div>
      </div>
    </div>

    <!-- content -->
    <div class="flex flex-col items-center pt-24 p-2">
      <slot />
    </div>
    
  </div>
  
</template>