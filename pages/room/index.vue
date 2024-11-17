<script setup>
import axios from 'axios';

const apiUrl = 'https://nuxr3.zeabur.app/api/v1/rooms';
const roomsList = ref([]);

// const { data } = await useAsyncData('roomList', async () => {
//     const res = await axios.get(apiUrl);

//     return res.data;
// });
const { data } = await useFetch(apiUrl);

roomsList.value = data.value.result;

// 使用 fetch 或 axios 串接 前台房型 API ( GET )
// apiUrl : https://nuxr3.zeabur.app/api/v1/rooms
// response 回傳後，將資料寫入 roomsList 變數
// 使用 roomsList 變數在下方 template 渲染列表
</script>

<template>
    <h1>房型頁面</h1>
    <div class="container mt-4">
        <div class="row justify-content-center">
            <NuxtLink
                class="col-8 col-md-6 col-lg-3"
                v-for="room in roomsList"
                :key="room._id"
                :to="`/room/${room._id}`"
            >
                <div class="card h-100 shadow-sm">
                    <img
                        :src="room.imageUrl"
                        class="card-img-top"
                        alt="Room Image"
                    />
                    <div class="card-body d-flex flex-column">
                        <h3 class="card-title">{{ room.name }}</h3>
                        <p class="card-text flex-grow-1">
                            {{ room.description }}
                        </p>
                        <ul class="list-unstyled">
                            <li><strong>面積:</strong> {{ room.areaInfo }}</li>
                            <li><strong>床型:</strong> {{ room.bedInfo }}</li>
                            <li>
                                <strong>最大容納人數:</strong>
                                {{ room.maxPeople }}
                            </li>
                            <li><strong>價格:</strong> {{ room.price }}</li>
                        </ul>
                    </div>
                </div>
            </NuxtLink>
        </div>
    </div>
</template>

<style scoped></style>
