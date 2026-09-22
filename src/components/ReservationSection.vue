<script setup>
import { ref } from 'vue'
const date = ref('')
const guests = ref('2 位')
const message = ref('')
function submitReservation() { message.value = date.value ? `已为您记录 ${date.value}、${guests.value} 的用餐意向，我们将尽快与您确认。` : '请选择用餐日期。' }
</script>
<template><section class="booking" id="booking"><p class="eyebrow">MAKE A RESERVATION</p><h2>留一席，<em>等你来。</em></h2><form @submit.prevent="submitReservation"><label>用餐日期<input v-model="date" aria-label="用餐日期" type="date" required></label><label>用餐人数<select v-model="guests" aria-label="用餐人数"><option>2 位</option><option>3 位</option><option>4 位</option><option>5 位以上</option></select></label><button type="submit">开始预约 <span>→</span></button></form><p class="booking-message" aria-live="polite">{{ message }}</p></section></template>
