<script setup>
  const route = useRoute();
  const router = useRouter();

  console.log(route);
  const gotoAndPage = (path) => {
    router.push({ path });
  };
</script>

<template>
  <div>
    <h1>首頁</h1>

    <NuxtLink to="/about">關於我們</NuxtLink>
    <NuxtLink to="/address">聯絡地址</NuxtLink>
    <NuxtLink to="/courses/123/about">課程列表</NuxtLink>
    <NuxtLink to="/user-mike">使用者頁面</NuxtLink>
  </div>
</template>

<style></style>
