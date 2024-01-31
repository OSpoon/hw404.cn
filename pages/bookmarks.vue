<template>
  <main class="min-h-screen">
    <AppHeader class="mb-8" title="收藏夹" :description="description" />
    <ul class="space-y-2">
      <li v-for="bookmark in bookmarks" :key="bookmark.id">
        <a
          :href="bookmark.url"
          target="_blank"
          class="flex items-center gap-3 hover:bg-gray-100 dark:hover:bg-white/10 p-2 rounded-lg -m-2 text-sm min-w-0"
        >
          <UAvatar
            :src="getThumbnail(bookmark.url)"
            :alt="bookmark.label"
            :ui="{ rounded: 'rounded-md' }"
          />
          <p class="truncate text-gray-700 dark:text-gray-200">
            {{ bookmark.label }}
          </p>
          <span class="flex-1"></span>
          <span class="text-xs font-medium text-gray-400 dark:text-gray-600">
            {{ getHost(bookmark.url) }}
          </span>
        </a>
      </li>
    </ul>
  </main>
</template>

<script setup>
const description = "";
useSeoMeta({
  title: "收藏夹 | 小鑫同学",
  description,
});

const bookmarks = [
  {
    id: 1,
    label: "HarmonyOS Developer",
    url: "https://developer.huawei.com/consumer/cn/",
  },
  {
    id: 2,
    label: "智谱清言",
    url: "https://chatglm.cn/",
  },
  {
    id: 3,
    label: "Monaco-editor 学习文档",
    url: "https://aydk.site/",
  },
  {
    id: 4,
    label: "Chrome for developers",
    url: "https://developer.chrome.com/docs/extensions?hl=zh-cn",
  },
  {
    id: 5,
    label: "ESLint 中文网",
    url: "https://eslint.nodejs.cn/",
  },
  {
    id: 6,
    label: "Quarkc，为跨技术栈而生！",
    url: "https://quarkc.hellobike.com/#/",
  },
  {
    id: 7,
    label: "LogicFlow 流程图编辑框架",
    url: "https://site.logic-flow.cn/",
  },
];

function getHost(url) {
  const parsedUrl = new URL(url);
  let host = parsedUrl.host;
  if (host.startsWith("www.")) {
    host = host.substring(4);
  }
  return host;
}

function getThumbnail(url) {
  const host = getHost(url);
  return `https://logo.clearbit.com/${host}`;
}
</script>
