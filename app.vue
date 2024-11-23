<script setup>
// import axios from 'axios';

// const { data, refresh } = await useFetch("https://nuxr3.zeabur.app/api/v1/rooms/");

// 多個 api 請求
const { data } = await useAsyncData("info", async () => {
  const apis = [
    $fetch(`https://nuxr3.zeabur.app/api/v1/rooms/`),
    $fetch(`https://nuxr3.zeabur.app/api/v1/rooms/66b6e81931c83030e03b537d`)
  ];

  const all = await Promise.allSettled(apis);

  // 只處理成功的請求結果
  const successfulResponses = all
    .filter(res => res.status === 'fulfilled') // 過濾出成功的結果
    .map(res => res.value); // 提取成功的資料

  return successfulResponses;
});

console.log(data.value);

// const refreshData = () => {
//   refresh();
// }
</script>

<template>
  <!-- <button @click="refreshData">重新抓取網頁資料</button> -->
  <!-- <div>{{ data[0].result }}</div> -->

  <div v-for="(item) in data[0].result" :key="_id">
    房間名：{{ item.name }}
    <br>
    描述：{{ item.description }}
    <hr>
  </div>
  
</template>
