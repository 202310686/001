<script setup>
defineProps({ links: { type: Array, required: true } })
</script>
<template><footer><a class="logo" href="#top"><span>山岚</span><i>SHANLAN</i></a><p>© 2024 SHANLAN SEASONAL KITCHEN</p><div><a v-for="link in links" :key="link" href="#">{{ link }}</a></div></footer></template>
