<template>
  <div>

<!--  Desktop version-->
  <div class="q-pr-xl q-pl-xl bg-grey-2 desktop-only" style="max-width: 100%; margin: 0 auto">

    <home-banners/>
    <br>
    <q-separator/>
    <br>
    <hot-trending-products/>
    <br>
    <q-separator/>
    <br>
    <popular-categories/>
    <br>
    <flash-deals/>
    <br>
    <home-banners-jr/>
    <br>
    <top-featured-products/>
    <br>
    <recommending-for-you/>
    <br>
    <blog/>
    <br>

    <home-footer/>

  </div>


<!--    Mobile Version-->
    <div class="q-pr-sm q-pl-sm bg-grey-2 mobile-only" style="max-width: 100%; margin: 0 auto">

      <home-banners/>
      <br>
      <hot-trending-products/>
      <br>
      <popular-categories/>
      <br>
      <flash-deals/>
      <br>
      <home-banners-jr/>
      <br>
      <top-featured-products/>
      <br>
      <recommending-for-you/>
      <br>
      <blog/>
      <br>

      <home-footer/>

    </div>
  </div>
</template>

<script>
import HomeBanners from "components/home/HomeBanners";
import HotTrendingProducts from "components/home/hot-trending/HotTrendingProducts";
import PopularCategories from "components/home/popular-categories/PopularCategories";
import HomeHeader from "components/home/HomeHeader";
import FlashDeals from "components/home/flash-deals/FlashDeals";
import HomeBannersJr from "components/home/HomeBannersJr";
import TopFeaturedProducts from "components/home/top-featured/TopFeaturedProducts";
import RecommendingForYou from "components/home/RecommendingForYou";
import Blog from "components/home/blog/Blog";
import HomeFooter from "components/home/HomeFooter";

export default {
  name: "HomePage",
  components: {
    HomeFooter,
    Blog,
    RecommendingForYou,
    TopFeaturedProducts,
    HomeBannersJr, FlashDeals, HomeHeader, PopularCategories, HotTrendingProducts, HomeBanners},
  data() {
    return {}
  }
}
</script>

<style scoped>

</style>
