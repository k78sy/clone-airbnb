<script setup>
// eslint-disable-next-line no-unused-vars
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
header{
  background: #EBEBEB;
background: linear-gradient(0deg, #EBEBEB 0%, #fff 100%);
}
</style>