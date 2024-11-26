<script setup></script>

<template>
  <div>
    <h2>關於我們</h2>

    <NuxtLink to="/">回到首頁</NuxtLink>
    <NuxtLink to="/address">聯絡地址</NuxtLink>

    <br>

    <div class="nav">
      <NuxtLink to="/about">about index</NuxtLink>
      <NuxtLink to="/about/a">about a</NuxtLink>
      <NuxtLink to="/about/b">about b</NuxtLink>
    </div>

    <div class="box_page">
      <NuxtPage></NuxtPage>
    </div>

  </div>
</template>

<style>
.nav>a {
  display: block;
  margin: 0 10px;
}

.box_page {
  width: 800px;
  height: 400px;
  background-color: #ddd;
}
</style>
