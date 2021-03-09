<template>
  <div>
    <h1>{{ result }}</h1>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'AsyncShow',
  setup() {
    return new Promise((resolve) => {
      setTimeout(() => {
        return resolve({
          result: '这是请求结果',
        })
      }, 3000)
    })
  },
})
</script>

<style>
</style>
