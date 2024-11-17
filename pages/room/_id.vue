<script setup>
const router = useRouter();
</script>

<template>
    <h2>房型詳細頁面</h2>
    <button type="button" class="btn" @click="router.go(-1)">前往上一頁</button>
</template>

<style lang="scss" scoped>
.btn {
    padding: 10px;
    margin: 10px 0;
    background: #fff;
}
</style>
