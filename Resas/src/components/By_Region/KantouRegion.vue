<template>
    <div class="ktRegion_style">
        <h2 class="regionName">関東地方</h2>
        <template v-for="prefecture in prefectures" :key="prefecture.prefCode">
            <CheckBox v-if="prefecture.prefCode >= 8 && prefecture.prefCode <= 14" 
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
.ktRegion_style{
    width: 100%;
    height: 70vh;
    display: flex;
    flex-direction: column;
}
.regionName{
    margin-left: 2rem;
}
</style>