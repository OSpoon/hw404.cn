<template>
  <div class="space-y-6">
    <UAvatar src="/avatar.png" alt="小鑫同学" size="3xl" />
    <h1
      class="text-xl font-bold tracking-tight text-gray-800 dark:text-gray-100"
    >
      👋 Hi, I'm 小鑫同学
    </h1>
    <p class="text-gray-900 dark:text-gray-400">
      我是一个乐于知识分享的程序员，业余期间在 掘金社区以ID
      <a
        target="_blank"
        href="https://juejin.cn/user/3966693685871694"
        class="underline"
        >[小鑫同学]
      </a>
      发布了 200 余篇技术文章，包含了框架教程、插件开发、案例实操等多个方面。
    </p>
    <p class="text-gray-900 dark:text-gray-400">
      最近两年主要负责公司 B 端产品升级以及维护，运用微前端（MicroApp）框架，以
      Angular8.x 与 Vuejs3.x 为主要技术构建，并逐步切换到 Vuejs。
    </p>
  </div>
</template>

<script setup>
useSeoMeta({
  title: "小鑫同学",
  description: "我是小鑫同学, 一个乐于知识分享的程序员",
});
</script>
