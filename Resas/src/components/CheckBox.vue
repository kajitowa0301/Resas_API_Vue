<template>
  <label class="check_label">
    <input type="checkbox" :id="prefCode" :name="prefName" :value="prefName" class="check_box">
    <span class="Prefecture_Name">{{ prefName }}</span>
  </label>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

const { prefCode, prefName } = defineProps(['prefCode', 'prefName',]);
</script>

<style scoped>
.check_label{
  margin: 0 0.9rem;
  padding-left: 1.2rem ;
}
.check_box {
  width: 1.2rem;
  height: 1.2rem;
}
.Prefecture_Name{
  font-size: 1.1rem;
  margin-left: 0.3rem;
}
</style>
