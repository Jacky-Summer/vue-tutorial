<template>
  <div>
    {{ count }}
    <button @click="changeCount">count加1</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, watch, ref } from 'vue'

export default defineComponent({
  setup() {
    const count = ref(0)
    const changeCount = () => {
      count.value++
    }
    watch(count, (newCount, prevCount) => {
      console.log('newCount:', newCount, ' oldCount:', prevCount)
    })

    return {
      count,
      changeCount,
    }
  },
})
</script>

<style>
</style>
