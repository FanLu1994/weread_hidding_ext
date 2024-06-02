<script setup lang="js">
import { useFavicon } from '@vueuse/core'
import { onMounted, ref } from 'vue'
import 'uno.css'
import '../../assets/feishu.png'
import FeishuShelf from '~/contentScripts/components/FeishuShelf.vue'

const bookList = ref([])

const icon = useFavicon()
icon.value = '../../assets/feishu.png'

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
        author: '夏目',
      },
    )
  }
})
</script>

<template>
  <div class="fixed w-full h-full right-0 bottom-0 z-100 flex items-end leading-1em">
    <FeishuShelf :book-list="bookList" />
  </div>
</template>
