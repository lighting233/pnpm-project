<template>
  <div class="menu">
    <page-content :content-config="contentConfig"></page-content>
  </div>
</template>

<script setup lang="ts" name="menu">
import pageContent from '@/components/page-content/page-content.vue'

import contentConfig from './config/content.config'
</script>

<style scoped>
.menu {
}
</style>
