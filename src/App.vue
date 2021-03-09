<template>
  <setup-demo></setup-demo>
  <ref-demo></ref-demo>
  <reactive-demo></reactive-demo>
  <to-ref-demo></to-ref-demo>
  <to-refs-demo></to-refs-demo>
  <computed-demo></computed-demo>
  <watch-demo></watch-demo>
  <watch-effect-demo></watch-effect-demo>
  <readonly-demo></readonly-demo>
  <teleport-demo></teleport-demo>
  <suspense-demo></suspense-demo>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import SetupDemo from './components/SetupDemo.vue'
import RefDemo from './components/RefDemo.vue'
import ReactiveDemo from './components/ReactiveDemo.vue'
import ToRefDemo from './components/ToRefDemo.vue'
import ToRefsDemo from './components/ToRefsDemo.vue'
import ComputedDemo from './components/ComputedDemo.vue'
import WatchDemo from './components/WatchDemo.vue'
import WatchEffectDemo from './components/WatchEffectDemo.vue'
import ReadonlyDemo from './components/ReadonlyDemo.vue'
import TeleportDemo from './components/TeleportDemo.vue'
import SuspenseDemo from './components/SuspenseDemo.vue'

export default defineComponent({
  name: 'App',
  components: {
    SetupDemo,
    RefDemo,
    ReactiveDemo,
    ToRefDemo,
    ToRefsDemo,
    ComputedDemo,
    WatchDemo,
    WatchEffectDemo,
    ReadonlyDemo,
    TeleportDemo,
    SuspenseDemo,
  },
})
</script>

<style>
</style>
