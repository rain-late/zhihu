<template>
  <ul>
    <li v-for="column in list" :key="column.id">
      <img :src="column.avatar" :alt="column.title" />
      <span>{{ column.title }}</span>
      <span>{{ column.description }}</span>
      <a href="#">进入专栏</a>
    </li>
  </ul>
</template>
<script lang="ts">
import { defineComponent, PropType } from 'vue'
export interface ColumnProps {
  id: number;
  title: string;
  avatar?: string;
  description: string;
}

export default defineComponent({
  name: 'ColumnList',
  props: {
    list: {
      type: Array as PropType<ColumnProps[]>,
      required: true,
      default: () => []
    }
  },
  setup (props) {
    props.list.forEach(item => {
      console.log(item.id)
    })
  }
})
</script>
