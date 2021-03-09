<template>
  <div>{{ foo }}</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    title: String,
  },
  setup() {
    // Composition API 逻辑组织的入口
    const foo = 2
    // console.log(this) // undefined
    // console.log(props.title, context)
    return {
      foo,
    }
  },
})
</script>

<style>
</style>
