<script setup>
import HeaderNav from '@/components/header/HeaderNav.vue'
import HeaderFilter from '@/components/header/HeaderFilter.vue'
</script>
<template>
  <header>
    <header-nav></header-nav>
    <header-filter></header-filter>
  </header>
</template>
<style lang="scss">
header {
  background: #ebebeb;
  background: linear-gradient(0deg, #ebebeb 0%, #fff 100%);
}
</style>
