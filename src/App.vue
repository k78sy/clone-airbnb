<script setup>
//import { RouterLink, RouterView } from 'vue-router'
import HeaderTop from '@/components/HeaderTop.vue'
import FooterBottom from '@/components/FooterBottom.vue'
import MainSection from '@/components/MainSection.vue'

import { onMounted, reactive } from 'vue' //{ 상수,변수,함수가 넘어온다 }
import axios from 'axios' //객체 주소값 리턴

const state = reactive({
  sections: [],
})

onMounted(async () => {
  axios.get('airbnb.json').then((res) => {
    state.sections = res.data.sections
    console.log(state.sections)
  })
})
</script>

<template>
  <header-top />
  <main-section />
  <footer-bottom />
</template>

<style scoped lang="scss"></style>
