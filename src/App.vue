<script setup>
//import { RouterLink, RouterView } from 'vue-router'
import HeaderTop from '@/components/HeaderTop.vue'
import FooterBottom from '@/components/FooterBottom.vue'
import SlideItem from '@/components/SlideItem.vue'

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
    <section v-for="section in state.sections" :key="section.sectionId">
    <div class="slider-top">
      <a href="">
        {{ section.sectionData.title }}
        <font-awesome-icon :icon="['fas', 'angle-right']" />
      </a>
      <div class="slider-button">
        <button class="arrow-btn btn-arctive">
          <font-awesome-icon :icon="['fas', 'angle-left']" />
        </button>
        <button class="arrow-btn">
          <font-awesome-icon :icon="['fas', 'angle-right']" />
        </button>
      </div>
    </div>
    <div class="slider-list">
      <slide-item
        v-for="item in section.sectionData.items"
        :key="item.demandStayListing.id"
        :picture="item.contextualPictures[0].picture"
        :title="item.title"
        :price="item.structuredDisplayPrice.primaryLine.accessibilityLabel"
        :period="item.structuredContent.primaryLine[0].body"
        :rating="item.avgRatingLocalized"
        :badge="item.badges.length ? item.badges[0].text: ''"
      />
    </div>
  </section>
  <footer-bottom />
</template>

<style scoped lang="scss"></style>
