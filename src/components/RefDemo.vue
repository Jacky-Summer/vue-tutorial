<template>
  <div>
    {{ count }}
    <button @click="handleClick">加1</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup() {
    // 被 ref 方法包裹后的元素就变成了一个代理对象
    const count = ref(0)

    const handleClick = () => {
      count.value++ // 在setup里面使用ref代理对象需要 `.value`，模板中使用时由于vue帮我们做了自动解析所以不用 `.value`
    }

    return {
      count,
      handleClick,
    }
  },
})
</script>

<style>
</style>
