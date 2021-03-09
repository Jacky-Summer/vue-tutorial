<template>
  <div>
    {{ foo }}
    {{ bar }}
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue'

export default defineComponent({
  setup() {
    // 创建一个响应式对象state
    const state = reactive({
      foo: 1,
      bar: 2,
    })

    const stateAsRefs = toRefs(state) // 将响应式的对象变为普通对象结构, 且能使用ES6的扩展运算符，也仍具有响应性

    // ref 和原始 property 已经“链接”起来了
    state.foo++
    console.log(stateAsRefs.foo.value) // 2

    stateAsRefs.foo.value++
    console.log(state.foo) // 3

    return {
      ...stateAsRefs,
    }
  },
})
</script>

<style>
</style>
