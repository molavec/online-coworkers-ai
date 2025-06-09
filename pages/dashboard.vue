<script setup lang="ts">
// No hay lógica específica aún
// Array bookmarks objects { id, name, url, icon }
const bookmarks = ref([
  { id: 1, name: 'Figma Project 1', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
  { id: 2, name: 'Figma Project 2', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
  { id: 3, name: 'Figma Project 3', url: 'https://static.figma.com/app/icon/1/favicon.png', icon: 'https://static.figma.com/app/icon/1/favicon.png' },
])

// Array task objects { id, title, description, user, status, createdAt, updatedAt, isCompleted }
const tasks = ref([
  { id: 1, title: 'Task 1', description: 'Description of Task 1', user: 'User 1', status: 'Pending', createdAt: new Date(), updatedAt: new Date(), isCompleted: false },
  { id: 2, title: 'Task 2', description: 'Description of Task 2', user: 'User 2', status: 'In Progress', createdAt: new Date(), updatedAt: new Date(), isCompleted: false },
  { id: 3, title: 'Task 3', description: 'Description of Task 3', user: 'User 3', status: 'Completed', createdAt: new Date(), updatedAt: new Date(), isCompleted: true },
])

</script>

<template>
  <div>
    <div class="w-full">
      
      <div class="flex items-center justify-end px-2">
        <UserBubble username="User 1" class="mr-[-10px] hover:z-100" />
        <UserBubble username="User 2" class="mr-[-10px] hover:z-100" />
        <UserBubble username="+" />
      </div>
  
      <div class="flex gap-4 w-full">
        <div class="w-full p-2">
          <!-- title -->
          <h1 class="text-2xl font-light mb-4">Quick Links</h1>
    
          <!-- content -->
          <div class="list rounded-box shadow bg-gray-800">
            <BookmarkItem 
              v-for="bookmark in bookmarks" 
              :id="bookmark.id" 
              :key="bookmark.id" 
              :name="bookmark.name" 
              :url="bookmark.url" 
              :icon="bookmark.icon"
              @delete="bookmarks.splice(bookmarks.indexOf(bookmark), 1)"
            />
          </div>
        </div>
        <div class="w-full p-2">
          <!-- title -->
          <h1 class="text-2xl font-light mb-4">Tasks</h1>
    
          <!-- content -->
          <div class="list rounded-box shadow bg-gray-800">
            <TaskItem
              v-for="task in tasks" 
              :id="task.id" 
              :key="task.id" 
              v-model="task.isCompleted"
              :title="task.title" 
              :description="task.description"
              @delete="tasks.splice(tasks.indexOf(task), 1)"
            />
            <!-- <div 
              v-for="task in tasks" 
              :key="task.id" 
              class="list-row flex items-center justify-between gap-4"
            >
              <div class="flex items-center gap-4 flex-grow">
                <input v-model="task.isCompleted" type="checkbox" class="checkbox" >
                <div>
                  <h1 class="text-lg">{{ task.title }}</h1>
                  <span class="text-xs">{{ task.description }}</span>
                </div>
              </div>
              <div class="px-2" @click.stop="tasks.splice(tasks.indexOf(task), 1)">
                <XCircleIcon class="size-6 cursor-pointer"/>
              </div>
            </div> -->
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<style scoped></style>
