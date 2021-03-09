<template>
  <div>
    {{ count }}
    <button @click="changeCount">count加1</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, watchEffect } from 'vue'

export default defineComponent({
  setup() {
    const count = ref(0)
    const changeCount = () => {
      count.value++
    }

    watchEffect(() => console.log(count.value))
    // -> logs 0

    setTimeout(() => {
      count.value++
      // -> logs 1
    }, 100)

    return {
      count,
      changeCount,
    }
  },
})
</script>

<style>
</style>
