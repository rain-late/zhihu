<template>
  <div class="container">
    <ColumnList :list="list"/>
  </div>
  <router-view/>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'

import ColumnList, { ColumnProps } from './components/ColumnList.vue'
const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test1的专栏',
    description: '这是test1的专栏，有一段非常有意思的简介，可以更新一下',
    avatar: 'https://dummyimage.com/100x100/8d8a99/ffffff'
  },
  {
    id: 2,
    title: 'test2的专栏',
    description: '这是test2的专栏，有一段非常有意思的简介，可以更新一下',
    avatar: 'https://dummyimage.com/100x100/8d8a99/ffffff'
  },
  {
    id: 3,
    title: 'test3的专栏',
    description: '这是test3的专栏，有一段非常有意思的简介，可以更新一下'
    // avatar: 'https://dummyimage.com/100x100/8d8a99/ffffff'
  },
  {
    id: 4,
    title: 'test4的专栏',
    description: '这是test4的专栏，有一段非常有意思的简介，可以更新一下',
    avatar: 'https://dummyimage.com/100x100/8d8a99/ffffff'
  }
]

export default defineComponent({
  name: 'App',
  components: {
    ColumnList
  },
  setup () {
    return {
      list: testData
    }
  }
})
</script>
<style>
</style>
