<template>
<div>

<!--  Desktop version-->
  <div class=" mobile-hide">
    <div class="row ">
      <div class="col-11 text-h6">Flash Deals</div>

    </div>
  <div>
    <div class="row">
<div class="q-pa-md col-6"><flash-deal-component/></div>
<div class="q-pa-md col-6"><flash-deal-component/></div>
    </div>
  </div>
  </div>

<!--  Mobile Version-->
  <div class="mobile-only desktop-hide">
    <div class="row ">
      <div class="col-11 text-h6">Flash Deals</div>

    </div>


    <div class="q-pa-md">
      <q-virtual-scroll
        :items="heavyList"
        virtual-scroll-horizontal

      >
        <template v-slot="{ item, index }">
          <div class="row no-wrap">
            <div style="width: 250px" class="q-pa-sm">

              <flash-deal-mobile-component :name="item.name" :image-src="item.imageSrc" :price="item.price" :max="item.max" :sold="item.sold" :rating="item.rating"   />

            </div>
          </div>
        </template>
      </q-virtual-scroll>
    </div>


  </div>
</div>
</template>

<script>
import FlashDealComponent from "components/home/flash-deals/FlashDealComponent";
import FlashDealMobileComponent from "components/home/flash-deals/FlashDealMobileComponent";
export default {
  name: "FlashDeals",
  components: {FlashDealMobileComponent, FlashDealComponent},
  data(){
    return {
      heavyList :[
        {
          imageSrc:'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/3/_/x3_1.jpg.pagespeed.ic.2IVvVUTpco.webp',
          name:'Somic G951 Gaming Headset',
          rating:4,
          price:80,
          sold : 35,
          max: 100,
        },
        {
          imageSrc:'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/4/_/4.jpg',
          name: 'Somic G951 Gaming Headset',
          rating:5,
          price:90,
          sold : 56,
          max: 100,
        },
        {
          imageSrc:'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/4/_/4.jpg',
          name: 'Somic G951 Gaming Headset',
          rating:5,
          price:90,
          sold : 56,
          max: 100,
        },
        {
          imageSrc:'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/4/_/4.jpg',
          name: 'Somic G951 Gaming Headset',
          rating:5,
          price:90,
          sold : 56,
          max: 100,
        },{
          imageSrc:'https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/4/_/4.jpg',
          name: 'Somic G951 Gaming Headset',
          rating:5,
          price:90,
          sold : 56,
          max: 100,
        },


      ]
    }
  }
}
</script>

<style scoped>

</style>
