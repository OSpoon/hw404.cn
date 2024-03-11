<template>
  <div>
    <h2 class="uppercase text-xs font-semibold text-gray-400 mb-4">工具地址</h2>
    <div class="flex flex-wrap gap-3">
      <UCard
        v-for="link in tools"
        :key="link.icon"
        :ui="{ ring: 'ring-0 ring-gray-200 dark:ring-gray-800' }"
      >
        <NuxtLink
          :to="link.url"
          target="_blank"
          external
          class="p-2 -m-2 rounded-lg dark:hover:text-gray-300"
        >
          <Icon :name="link.icon" class="w-6 h-6 mr-2"></Icon>
          <span class="text-sm">
            {{ link.name }}
          </span>
        </NuxtLink>
      </UCard>
    </div>
  </div>
</template>

<script lang="ts" setup>
const tools = [
  {
    name: "Stackblitz",
    url: "https://stackblitz.com/",
    icon: "simple-icons:stackblitz",
  },
  {
    name: "Codesandbox",
    url: "https://codesandbox.io/",
    icon: "simple-icons:codesandbox",
  },
  {
    name: "TransformTools",
    url: "https://transform.tools/",
    icon: "material-symbols-light:transform-rounded",
  },
  {
    name: "智普清言",
    url: "https://chatglm.cn/",
    icon: "bi:chat-dots",
  },
  {
    name: "Regex101",
    url: "https://regex101.com/",
    icon: "mdi:regex",
  },
  {
    name: "IT-TOOLS",
    url: "https://it-tools.tech/",
    icon: "carbon:tools",
  },
];
</script>
