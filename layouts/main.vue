<script setup lang="ts">
import WorkspacesLogo from '~/components/WorkspacesLogo.vue'
</script>
<template>
  <div>
    <!-- header -->
    <div class="flex items-center justify-between bg-queonda-500 p-4">
      <div class="left">
        <WorkspacesLogo />
      </div>
      <div class="right">
        <div class="avatar avatar-placeholder">
          <div class="bg-neutral text-neutral-content w-12 rounded-full">
            <span>SY</span>
          </div>
        </div>
      </div>
    </div>

    <!-- content -->
    <div class="flex flex-col items-center pt-28 p-4">
      <slot />
    </div>
    
  </div>
  
</template>