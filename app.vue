<script setup>
import axios from 'axios';

// const { data, refresh } = await useFetch("https://nuxr3.zeabur.app/api/v1/rooms/");

const { data, refresh } = await useAsyncData("index", async () => {
  const res = await axios.get("https://nuxr3.zeabur.app/api/v1/rooms/");
  return res.data;
})

const refreshData = () => {
  refresh();
}

</script>

<template>
  <button @click="refreshData">重新抓取網頁資料</button>

  <div>{{ data }}</div>
</template>
