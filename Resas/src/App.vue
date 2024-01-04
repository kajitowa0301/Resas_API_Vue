<template>
    <div>
        <h1>都道府県一覧</h1>
        <HokkaidoTohokuRegion></HokkaidoTohokuRegion>
    </div>
</template>

<script setup lang="ts">
import { onMounted, ref, provide } from 'vue';
import axios from 'axios';
import type { Prefecture } from './interfaces';
import HokkaidoTohokuRegion from './components/HokkaidoTohokuRegion.vue';

const prefectures = ref<Prefecture[]>([]);
provide("prefectures", prefectures);

const apiKey = 'rhzarpFNCEuH6b6PyxVrMr4xcuQjsWe6DGN56Akd';

const fetchPrefectures = async () => {
    try {
        const response = await axios.get('https://opendata.resas-portal.go.jp/api/v1/prefectures', {
            headers: {
                'X-API-KEY': apiKey,
            },
        });
        prefectures.value = response.data.result; 
    } catch (error) {
        console.error('Error fetching prefectures:', error);
    }
};

onMounted(() => {
    fetchPrefectures();
});
</script>

