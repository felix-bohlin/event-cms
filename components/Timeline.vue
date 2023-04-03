<script setup lang="ts">
defineProps<{
  timelineItems: {
    id: number
    description: string
    icon: "default"
    title: string
  }[]
  title?: string
}>()

const isEditing = useIsEditing()
</script>

<template>
  <section :class="isEditing ? 'is-editing' : ''">
    <h2>{{ title }}</h2>

    <ul>
      <li v-for="item in timelineItems" :key="item.id">
        <span>{{ item.icon }}</span>
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
      </li>
    </ul>
  </section>
</template>
