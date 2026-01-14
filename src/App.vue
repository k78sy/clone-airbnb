<script setup>
//import { RouterLink, RouterView } from 'vue-router'
import HeaderTop from '@/components/HeaderTop.vue'
import FooterBottom from '@/components/FooterBottom.vue'
import SlideItem from '@/components/SlideItem.vue'

import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import { Navigation } from 'swiper/modules';
const modules = [Navigation]
import 'swiper/css/navigation';

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
  <section v-for="section in state.sections" :key="section.sectionData.loggingContext.backendSearchId">
    <div class="slider-top">
      <a href="">
        {{ section.sectionData.title }}
        <font-awesome-icon :icon="['fas', 'angle-right']" />
      </a>

      <div class="slider-button">
        <button :class="['prev-'+section.sectionData.loggingContext.backendSearchId]" class="arrow-btn">
          <font-awesome-icon :icon="['fas', 'angle-left']" />
        </button>
        <button :class="['next-'+section.sectionData.loggingContext.backendSearchId]" class="arrow-btn">
          <font-awesome-icon :icon="['fas', 'angle-right']" />
        </button>
      </div>
    </div>
    <swiper
    class="slider-list"
    :modules="modules"
    :slides-per-view="7"
    :space-between="10"
    :navigation="{
        nextEl: '.next-'+ section.sectionData.loggingContext.backendSearchId,
        prevEl: '.prev-'+ section.sectionData.loggingContext.backendSearchId,
      }"
    >
      <swiper-slide v-for="item in section.sectionData.items" :key="item.demandStayListing.id">
        <slide-item
          :picture="item.contextualPictures[0].picture"
          :title="item.title"
          :price="item.structuredDisplayPrice.primaryLine.accessibilityLabel"
          :period="item.structuredContent.primaryLine[0].body"
          :rating="item.avgRatingLocalized"
          :badge="item.badges.length ? item.badges[0].text : ''"
        />
      </swiper-slide>
    </swiper>
  </section>
  <footer-bottom />
</template>

<style scoped lang="scss"></style>
