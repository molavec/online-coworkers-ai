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
    <div class="flex gap-2 min-h-96 p-4">
      <!-- sidebar -->
      <div class="flex flex-col gap-2 p-4 min-w-42 border-r-2 border-queonda-400 min-h-full">
        <NuxtLink to="/dashboard" class="rounded-2xl p-2 bg-gray-800 shadow-xs shadow-red-600">Dashboard</NuxtLink>
        <NuxtLink to="/bookmarks" class="rounded-2xl p-2">Bookmarks</NuxtLink>
        <NuxtLink to="/tasks" class="rounded-2xl p-2">Tasks</NuxtLink>
      </div>
      <slot />
    </div>
  </div>
</template>