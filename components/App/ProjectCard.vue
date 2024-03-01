<template>
  <UCard :ui="{ ring: 'ring-0 ring-gray-200 dark:ring-gray-800' }">
    <NuxtLink
      class="flex justify-between p-2 -m-2 rounded-lg"
      :to="project.url"
      target="_blank"
      external
    >
      <div class="max-w-sm">
        <h3 class="text-sm font-medium group-hover:text-primary-600">
          {{ project.name }}
        </h3>
        <p class="text-gray-400 text-sm">{{ project.description }}</p>
      </div>
      <UAvatar
        :src="project.thumbnail"
        :ui="{ rounded: 'rounded z-10 relative' }"
        size="md"
        :alt="project.name"
      />
    </NuxtLink>
  </UCard>
</template>

<script setup>
defineProps({
  project: {
    type: Object,
    required: true,
  },
});
</script>
