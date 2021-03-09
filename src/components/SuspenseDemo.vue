<template>
  <div>
    <Suspense>
      <template #default>
        <!-- 请求成功展示 -->
        <async-show />
      </template>
      <template #fallback>
        <!-- 请求中和失败展示 -->
        <h2>Promise Loading...（请求中）</h2>
      </template>
    </Suspense>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AsyncShow from './AsyncShow.vue'

export default defineComponent({
  components: {
    AsyncShow,
  },
  setup() {
    //
  },
})
</script>

<style>
</style>
