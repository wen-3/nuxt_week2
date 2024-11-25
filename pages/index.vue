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
  </div>
  <hr>
  <button @click="gotoAndPage('/about')">切換至 about 頁面</button>
</template>

<style scoped></style>
