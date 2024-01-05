<template>
    <div class="htRegion_style">
        <h2>北海道・東北地方</h2>
        <template v-for="prefecture in prefectures" :key="prefecture.prefCode">
            <CheckBox v-if="prefecture.prefCode >= 1 && prefecture.prefCode <= 7" :prefCode="prefecture.prefCode"
                :prefName="prefecture.prefName"></CheckBox>
        </template>
    </div>
</template>

<script setup lang="ts">
import { inject } from 'vue';
import type { Prefecture } from '@/interfaces';
import CheckBox from '@/components/CheckBox.vue';


const prefectures = inject("prefectures") as Prefecture[];
</script>

<style scoped>
.htRegion_style{
    width: 100%;
    height: 70vh;
    display: flex;
    flex-direction: column;
}
</style>
