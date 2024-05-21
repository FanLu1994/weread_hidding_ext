<script setup lang="js">
import { useToggle } from '@vueuse/core'
import { onMounted, ref } from 'vue'
import 'uno.css'

const [show, toggle] = useToggle(false)
const bookList = ref([])

onMounted(() => {
  const ele = document.getElementsByClassName('shelf_list')
  if (!ele)
    return

  document.getElementById('app').style.display = 'none'

  // 找到ele中所有a标签
  const shelfEle = ele[0]
  const aList = shelfEle.getElementsByTagName('a')
  for (let i = 0; i < aList.length; i++) {
    const a = aList[i]
    // 获取图片的src
    const imgSrc = a.querySelector('.wr_bookCover_img').src
    // 获取标题
    const title = a.querySelector('.title').textContent
    const href = a.href
    bookList.value.push(
      {
        href,
        img: imgSrc,
        title,
      },
    )
  }
})
</script>

<template>
  <div class="fixed w-full h-full right-0 bottom-0 z-100 flex items-end font-sans leading-1em">
    <div class="shelf-container">
      <div v-for="item in bookList" :key="item.href" class="text-black">
        {{ item }}
      </div>
    </div>

    <div
      class="bg-white text-gray-800 rounded-lg shadow w-max h-min"
      p="x-4 y-2"
      m="y-auto r-2"
      transition="opacity duration-300"
      :class="show ? 'opacity-100' : 'opacity-0'"
    >
      <h1 class="text-lg">
        我自己的页面
      </h1>
      <SharedSubtitle />
    </div>
    <button
      class="flex w-10 h-10 rounded-full shadow cursor-pointer border-none"
      bg="teal-600 hover:teal-700"
      @click="toggle()"
    >
      <pixelarticons-power class="block m-auto text-white text-lg" />
    </button>
  </div>
</template>
