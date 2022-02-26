<template>
  <div>
<!--    <home-page/>-->
<!--    <product-detail-page/>-->
    <blog-page/>
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import HomePage from "pages/HomePage";
import ProductDetailPage from "pages/ProductDetailPage";
import BlogPage from "pages/BlogPage";

export default defineComponent({
  name: 'PageIndex',
  components: {BlogPage, ProductDetailPage, HomePage}
})
</script>
