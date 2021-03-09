<template>
  <div>
    {{ obj1.count1 }}
    {{ count2 }}
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue'

export default defineComponent({
  setup() {
    const obj1 = reactive({
      count1: 10,
    })
    const obj2 = reactive({
      count2: 20,
    })
    console.log(obj1)
    return {
      obj1,
      ...toRefs(obj2),
    }
  },
})
</script>

<style>
</style>
