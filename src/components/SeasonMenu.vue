<script setup>
defineProps({ dishes: { type: Array, required: true } })
</script>
<template><section class="season" id="menu"><div class="section-top"><p class="eyebrow">THIS SEASON</p><p class="section-count">01 / 03</p></div><div class="season-layout"><div class="season-title"><h2>秋日<br><em>食事</em></h2><p>以江南秋味为灵感<br>一口尝尽时令丰盈</p></div><article v-for="dish in dishes" :key="dish.name" class="menu-card" :class="dish.className"><div class="dish-art"><span></span><b></b><i></i></div><p class="dish-tag">{{ dish.type }}</p><h3>{{ dish.name }}</h3><p class="price">{{ dish.price }}</p></article></div><a class="all-menu" href="#booking">查看完整菜单 <span>↗</span></a></section></template>
