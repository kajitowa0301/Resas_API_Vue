<template>
    <div>
        <template v-for="prefecture in prefectures" :key="prefecture.prefCode">
            <CheckBox v-if="prefecture.prefCode >= 1 && prefecture.prefCode <= 7" :prefCode="prefecture.prefCode"
                :prefName="prefecture.prefName" :Name="prefecture.prefName"></CheckBox>
        </template>
    </div>
</template>

<script setup lang="ts">
import { inject } from 'vue';
import type { Prefecture } from '../interfaces';
import CheckBox from './CheckBox.vue';

const prefectures = inject("prefectures") as Prefecture[];
console.log(prefectures);

</script>

<style scoped></style>
