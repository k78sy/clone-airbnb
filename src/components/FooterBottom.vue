<script setup>
import FooterInfo from '@/components/footer/FooterInfo.vue'
import FooterRecommend from '@/components/footer/FooterRecommend.vue'
</script>
<template>
  <footer>
    <footer-recommend></footer-recommend>
    <footer-info></footer-info>
  </footer>
</template>
<style lang="scss">
footer {
  max-width: $width-pc;
  background: $gray;
  padding: 0 $pd 100px;
}
</style>
