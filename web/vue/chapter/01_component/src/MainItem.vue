<template>
  <!-- 页面中间内容 -->
  <div class="main-item">
    <main-banner></main-banner>
    <main-product-list></main-product-list>
  </div>
</template>

<script>
    import MainBanner from './MainBanner.vue';
    import MainProductList from './MainProductList.vue';

    export default {
        component: {
            MainBanner,
            MainProductList,
        },
    };
</script>
