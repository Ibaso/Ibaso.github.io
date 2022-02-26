<template>
<div>

<!--  Desktop Version-->
  <div class="mobile-hide">
    <div class="col-11 text-h6">Top Featured Products</div>

    <div class="row">
      <div class="col-5  q-pa-md">
        <flash-deal-component/>
      </div>
      <div class="col-7">
        <div class="row">
          <div v-for="item in heavyList" class="col-4 q-pa-md">
            <mini-flash-deals :name="item.name" :image-src="item.imageSrc" :rating="item.rating" :content="item.content" :price="item.price"/>
          </div>
        </div>


      </div>
    </div>
  </div>
<!--  Mobile Version-->
  <div class="desktop-hide">
    <div class="col-11 text-h6">Top Featured Products</div>

    <div class="row">
      <div v-for="item in heavyList" class="col-12 q-pa-md">
        <mini-flash-deals :name="item.name" :image-src="item.imageSrc" :rating="item.rating" :content="item.content" :price="item.price"/>
      </div>
    </div>
  </div>

</div>
</template>

<script>
import FlashDealComponent from "components/home/flash-deals/FlashDealComponent";
import TrendingProductCard from "components/home/hot-trending/TrendingProductCard";
import MiniFlashDeals from "components/home/MiniFlashDealsComponent";
import {computed} from "vue";
export default {
  name: "TopFeaturedProducts",
  components: {MiniFlashDeals, TrendingProductCard, FlashDealComponent},
  data(){
    return{
      heavyList: [
        {
          id: 1,
          name:'Unlocked Galaxy Mobile Phone',
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/c6954f6b4decd5efcd20abe057a6ba2a/3/0/x30_1.jpg.pagespeed.ic.DvXUcPo9_o.jpg',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 129
        },
        {
          id: 1,
          name:'A80 Pro 4G Cell Phone',
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/c6954f6b4decd5efcd20abe057a6ba2a/1/2/x12.jpg.pagespeed.ic.Xwi8vacDaL.jpg',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 82
        },
        {
          id: 1,
          name:'Golden Sheeps Case Compitable Pro',
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/c6954f6b4decd5efcd20abe057a6ba2a/3/1/x31.jpg.pagespeed.ic.sbc47s-2jc.jpg',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 336
        },
        // {
        //   id: 1,
        //   name:'iPhone 12 Pro Max Gold Edition',
        //   imageSrc: 'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/c6954f6b4decd5efcd20abe057a6ba2a/1/4/x14.jpg.pagespeed.ic.Hdo9Pj6lVI.jpg',
        //   rating: 4,
        //   content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
        //   price: 299
        // },
        // {
        //   id: 1,
        //   name:'Powered Quad Camera and Android',
        //   imageSrc: 'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/c6954f6b4decd5efcd20abe057a6ba2a/2/7/x27.jpg.pagespeed.ic.EnUJ4Nqz9X.jpg',
        //   rating: 4,
        //   content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
        //   price: 159
        // },
        // {
        //   id: 1,
        //   name:'Smart Watch for iOs Phones Proof',
        //   imageSrc: 'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/c6954f6b4decd5efcd20abe057a6ba2a/8/_/x8.jpg.pagespeed.ic.4Yh3zMvJKe.jpg',
        //   rating: 4,
        //   content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
        //   price: 240
        // },




      ]

    }
  },
  computed :{
    splicedList(){
      console.log(this.heavyList.splice(2,3))
      return []
    }
  }
}
</script>

<style scoped>

</style>
