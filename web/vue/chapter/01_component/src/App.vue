<template>
<!-- 页面头部内容 -->
  <div class="app">
    <HeaderItem></HeaderItem>
    <MainItem></MainItem>
    <FooterItem></FooterItem>
  </div>
</template>

<script>
import HeaderItem  from './HeaderItem.vue';
import MainItem  from './MainItem.vue';
import FooterItem from './FooterItem.vue';

export default {
  component: {
    HeaderItem,
    MainItem,
    FooterItem,
  }
}
</script>

<style>
.header-item, .main-item, .footer-item {
  border: 1px solid #999;
  margin-bottom: 4px;
}
</style>
