<template>
  <div ref="container"></div>
</template>

<script setup lang="ts">
import { onMounted, ref } from "vue"
const container = ref()
const options = {
  h5pJsonPath:  '/public/VideoIntroduce',
  frameJs: 'public/player/frame.bundle.js',
  frameCss: 'public/player/styles/h5p.css',
}
onMounted(() => {
  new H5PStandalone.H5P(container.value, options);
})
</script>
