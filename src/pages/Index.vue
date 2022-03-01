<template>
  <div>
<!--    <home-page/>-->
<!--    <product-detail-page/>-->
    <blog-page/>
<!--    <create-account-page/>-->
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import HomePage from "pages/HomePage";
import ProductDetailPage from "pages/ProductDetailPage";
import BlogPage from "pages/BlogPage";
import CreateAccountPage from "pages/client-admin/CreateAccountPage";

export default defineComponent({
  name: 'PageIndex',
  components: {CreateAccountPage, BlogPage, ProductDetailPage, HomePage}
})
</script>
