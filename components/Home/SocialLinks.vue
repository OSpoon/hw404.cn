<template>
  <div>
    <h2 class="uppercase text-xs font-semibold text-gray-400 mb-4">社区链接</h2>
    <div class="flex flex-wrap gap-3">
      <UCard
        v-for="link in links"
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
const links = [
  {
    name: "GitHub",
    url: "https://github.com/ospoon",
    icon: "mdi:github",
  },
  {
    name: "掘金",
    url: "https://juejin.cn/user/3966693685871694",
    icon: "simple-icons:juejin",
  },
  {
    name: "Gitpod",
    url: "https://gitpod.io/",
    icon: "simple-icons:gitpod",
  },
  {
    name: "Vercel",
    url: "https://vercel.com/",
    icon: "simple-icons:vercel",
  },
  {
    name: "Netlify",
    url: "https://www.netlify.com/",
    icon: "simple-icons:netlify",
  },
  {
    name: "Vite",
    url: "https://vitejs.dev/",
    icon: "simple-icons:vite",
  },
  {
    name: "Vue.js",
    url: "https://v3.cn.vuejs.org/",
    icon: "mdi:vuejs",
  },
  {
    name: "Ant Design Vue",
    url: "https://antdv.com/",
    icon: "simple-icons:antdesign",
  },
];
</script>
