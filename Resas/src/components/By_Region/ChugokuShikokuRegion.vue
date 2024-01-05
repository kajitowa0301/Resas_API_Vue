<template>
    <div class="csRegion_style">
        <h2>中国・四国地方</h2>
        <template v-for="prefecture in prefectures" :key="prefecture.prefCode">
            <CheckBox v-if="prefecture.prefCode >= 31 && prefecture.prefCode <= 39" 
                :prefCode="prefecture.prefCode" :prefName="prefecture.prefName"></CheckBox>
        </template>
    </div>
</template>

<script setup lang="ts">
import { inject } from 'vue';
import type { Prefecture } from '@/interfaces';
import CheckBox from '@/components/CheckBox.vue';

const prefectures = inject('prefectures') as Prefecture[];
</script>

<style scoped>
.csRegion_style{
    width: 100%;
    height: 70vh;
    display: flex;
    flex-direction: column;
}
</style>