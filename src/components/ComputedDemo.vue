<template>
  <div></div>
</template>

<script lang="ts">
import { defineComponent, ref, computed } from 'vue'

export default defineComponent({
  setup() {
    // const count = ref(1)
    // const plusOne = computed(() => count.value + 1) // 结果是一个 ref 代理对象，取值需要 .value

    // console.log(plusOne.value) // 2

    const count = ref(1)
    const plusOne = computed({
      get: () => count.value + 1,
      set: (val) => {
        count.value = val - 1
      },
    })

    plusOne.value = 1
    console.log(count.value) // 0
  },
})
</script>

<style>
</style>
