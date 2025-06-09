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
    <div>
      <slot />
    </div>
    
  </div>
  
</template>