<script setup>
defineProps({ links: { type: Array, required: true } })
</script>
<template>
  <header class="nav">
    <a class="logo" href="#top" aria-label="山岚食集首页"><span>山岚</span><i>SHANLAN</i></a>
    <nav aria-label="主导航"><a v-for="link in links" :key="link.label" :class="{ active: link.active }" :href="link.href">{{ link.label }}</a></nav>
    <a class="reserve reserve-small" href="#booking">预约一席 <span>↗</span></a>
  </header>
</template>
