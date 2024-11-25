<script setup>
const id = ref();
const router = useRouter();

const gotoAndPage = (path) => {
    router.push({ path });
    id.value = '';
};
</script>

<template>
    <input type="text" v-model="id">
    <button @click="gotoAndPage(`/courses/${id}`)">切換至單一課程</button>
    <hr>
    <NuxtPage></NuxtPage>
</template>

<style></style>