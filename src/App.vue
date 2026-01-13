<script setup>
//import { RouterLink, RouterView } from 'vue-router'
import HeaderTop from '@/components/HeaderTop.vue'
import FooterBottom from '@/components/FooterBottom.vue'
import ListSlider from '@/components/ListSlider.vue'

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
  <header-top></header-top>

  <main>
    <section v-for="section in state.sections" :key="section.sectionId">
      <div class="slider-top">
        <a href="">{{ section.sectionData.title }}</a>
        <div class="slider-button">
          <button class="arrow-btn btn-arctive">
            <font-awesome-icon :icon="['fas', 'angle-left']" />
          </button>
          <button class="arrow-btn"><font-awesome-icon :icon="['fas', 'angle-right']" /></button>
        </div>
      </div>
      <list-slider :foo="section.sectionData"></list-slider>
    </section>
  </main>



  <footer-bottom></footer-bottom>
</template>

<style scoped lang="scss"></style>
