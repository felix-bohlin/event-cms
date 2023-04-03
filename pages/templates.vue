<script setup lang="ts">
const isEditing = useIsEditing()
</script>

<template>
  <button type="button" @click="isEditing = !isEditing">
    <span v-if="isEditing">Save</span>
    <span v-else>Edit</span>
  </button>

  <Timeline
    :timelineItems="[
      {
        id: 1,
        title: 'First item',
        description: 'This is the first item',
        icon: 'default',
      },
      {
        id: 2,
        title: 'Second item',
        description: 'This is the second item',
        icon: 'default',
      },
    ]"
    title="Timeline"
  />
</template>
