<template>
  <div class="user-card">
    <b> {{ name }} </b>
    <button @click="isModalOpen = true">删除用户</button>

    <!-- 注意这一块代码 -->
    <Teleport to="#modal">
      <div v-show="isModalOpen">
        <p>确定删除?</p>
        <button @click="removeUser">确定</button>
        <button @click="isModalOpen = false">取消</button>
      </div>
    </Teleport>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from 'vue'

export default defineComponent({
  setup() {
    const isModalOpen = ref(false)
    const user = reactive({
      name: 'jacky',
    })

    const removeUser = () => {
      console.log('removeUser')
    }

    return {
      isModalOpen,
      removeUser,
      ...toRefs(user),
    }
  },
})
</script>

<style>
</style>
