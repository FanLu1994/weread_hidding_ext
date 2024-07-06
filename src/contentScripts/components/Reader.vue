<script setup lang="js">
import { onMounted, ref } from 'vue'

const ReaderRef = ref(null)

onMounted(() => {
  setTimeout(() => {
    const renderContainer = document.getElementsByClassName('wr_canvasContainer')
    if (renderContainer.length === 0) {
      console.error('wr_canvasContainer not found')
      return
    }
    const canvasList = renderContainer[0].getElementsByTagName('canvas')

    if (ReaderRef.value) {
      for (let i = 0; i < canvasList.length; i++)
        ReaderRef.value.appendChild(canvasList[1])

      // ReaderRef.value.appendChild(canvasList[1])
    }
  }, 2000)
})
</script>

<template>
  <div style="width: 100vw;height: 100vh;overflow:scroll;z-index: 100;background: white">
    <h1>Reader11111111111111111111</h1>
    <div id="reader-container" ref="ReaderRef" />
  </div>
</template>

<style scoped>

</style>
