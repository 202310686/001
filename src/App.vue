<script setup>
import SiteHeader from './components/SiteHeader.vue'
import HeroSection from './components/HeroSection.vue'
import SeasonMenu from './components/SeasonMenu.vue'
import StorySections from './components/StorySections.vue'
import ReservationSection from './components/ReservationSection.vue'
import SiteFooter from './components/SiteFooter.vue'

const navigation = [{ label: '菜单', href: '#menu', active: true }, { label: '食集', href: '#story' }, { label: '空间', href: '#space' }]
const dishes = [{ type: 'STARTER', name: '桂花酒酿\n炙甜虾', price: '68', className: 'card-one' }, { type: 'MAIN', name: '板栗菌菇\n焖土鸡', price: '128', className: 'card-two' }]
const socialLinks = ['小红书', '微信', 'Instagram']
</script>
<template><div class="grain"></div><SiteHeader :links="navigation" /><main><HeroSection /><SeasonMenu :dishes="dishes" /><StorySections /><ReservationSection /></main><SiteFooter :links="socialLinks" /></template>
