<template>
  <div></div>
</template>

<script lang="ts">
import { defineComponent, reactive, readonly, watchEffect } from 'vue'

export default defineComponent({
  setup() {
    const original = reactive({ count: 0 })

    // 返回的 readonly 对象，一旦修改就会在 console 有 warning 警告。程序还是会照常运行，不会报错。
    const copy = readonly(original)

    watchEffect(() => {
      // 只要有数据变化，这个函数都会执行
      console.log(copy.count)
    })

    // 这里会触发 watchEffect
    original.count++

    // 这里不会触发上方的 watchEffect，因为是 readonly。
    // copy.count++ // warning!
  },
})
</script>

<style>
</style>
