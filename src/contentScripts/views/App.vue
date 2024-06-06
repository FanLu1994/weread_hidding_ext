<script setup lang="js">
import { useBrowserLocation } from '@vueuse/core'
import { onMounted } from 'vue'
import 'uno.css'
import '../../assets/feishu.png'
import FeishuShelf from '~/contentScripts/components/FeishuShelf.vue'
import Reader from '~/contentScripts/components/Reader.vue'

const location = useBrowserLocation()

const path = computed(() => {
  // console.log(location.value)
  return location.value.pathname
})

onMounted(() => {

})
</script>

<template>
  <div class="fixed w-full h-full right-0 bottom-0 z-100 flex items-end leading-1em">
    <FeishuShelf v-if="path === '/web/shelf'" />
    <Reader v-else />
  </div>
</template>
