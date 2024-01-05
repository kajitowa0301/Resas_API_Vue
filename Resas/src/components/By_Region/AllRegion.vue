<template>
    <div class="position_style">
        <HokkaidoTohokuRegion></HokkaidoTohokuRegion>
        <KantouRegion></KantouRegion>
        <ChubuRegion></ChubuRegion>
        <KansaiRegion></KansaiRegion>
        <ChugokuShikokuRegion></ChugokuShikokuRegion>
        <KyushuRegion></KyushuRegion>        
    </div>
</template>

<script setup lang="ts">
import HokkaidoTohokuRegion from './HokkaidoTohokuRegion.vue';
import KantouRegion from './KantouRegion.vue';
import ChubuRegion from './ChubuRegion.vue';
import KansaiRegion from './KansaiRegion.vue';
import ChugokuShikokuRegion from './ChugokuShikokuRegion.vue';
import KyushuRegion from './KyushuRegion.vue';
</script>
<style scoped>
.position_style{
    width: 100%;
    height: 40vh;
    display: flex;
}
</style>