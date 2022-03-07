<template>
  <div>
    <home-page/>
<!--    <product-detail-page/>-->
<!--    <blog-page/>-->
<!--    <create-account-page/>-->
<!--    <customer-login-page/>-->
<!--    <admin-page/>-->
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import HomePage from "pages/HomePage";
import ProductDetailPage from "pages/ProductDetailPage";
import BlogPage from "pages/BlogPage";
import CreateAccountPage from "pages/client-admin/CreateAccountPage";
import CustomerLoginPage from "pages/client-admin/CustomerLoginPage";
import AdminPage from "pages/client-admin/AdminPage";

export default defineComponent({
  name: 'PageIndex',
  components: {AdminPage, CustomerLoginPage, CreateAccountPage, BlogPage, ProductDetailPage, HomePage}
})
</script>
