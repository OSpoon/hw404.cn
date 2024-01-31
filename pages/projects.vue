<template>
  <main class="min-h-screen">
    <AppHeader class="mb-12" title="项目集" :description="description" />
    <div class="space-y-4">
      <AppProjectCard
        v-for="(project, id) in projects"
        :key="id"
        :project="project"
      />
    </div>
  </main>
</template>

<script setup>
const description = "";
useSeoMeta({
  title: "项目集 | 小鑫同学",
  description,
});

const { data: projects } = await useAsyncData("projects-all", () =>
  queryContent("/projects").find()
);
</script>
