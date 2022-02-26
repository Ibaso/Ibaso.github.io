<template>
  <div class="row">

<!--    Banner for desktop-->
    <div class=" col-6 q-pa-sm mobile-hide">

      <q-carousel
        animated
        v-model="slide"
        transition-prev="slide-right"
        transition-next="slide-left"
        arrows
        navigation
        infinite
        style="border-radius: 20px"
        height="400px"
      >
        <q-carousel-slide :name="1"
                          img-src="https://www.centrumxp.pl/api/Images/Publikacje/lead_060220191544_129232.jpg"/>
        <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg"/>
        <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg"/>
        <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg"/>
      </q-carousel>
    </div>

<!--    Banner for Mobile-->
    <div class="col-12 q-pa-sm desktop-hide ">

      <q-carousel
        animated
        v-model="slide"
        transition-prev="slide-right"
        transition-next="slide-left"
        arrows
        navigation
        infinite
        style="border-radius: 20px"
        height="400px"
      >
        <q-carousel-slide :name="1"
                          img-src="https://www.centrumxp.pl/api/Images/Publikacje/lead_060220191544_129232.jpg"/>
        <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg"/>
        <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg"/>
        <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg"/>
      </q-carousel>
    </div>


    <div class="col-3 mobile-hide ">

      <div class="row q-pa-sm">
        <q-img src="https://cdn.quasar.dev/img/parallax2.jpg"
               style="border-radius: 20px"
               height="200px">
          >
          <div class="absolute-bottom text-subtitle2 text-center">
            Title
          </div>
        </q-img>
      </div>

      <div class="row q-pa-sm">
        <q-img src="https://cdn.quasar.dev/img/parallax2.jpg"
               style="border-radius: 20px"
               height="200px">
          >
          <div class="absolute-bottom text-subtitle2 text-center">
            Title
          </div>
        </q-img>
      </div>

    </div>

    <div class="col-3 mobile-hide">

      <div class="row q-pa-sm">
        <q-img src="https://cdn.quasar.dev/img/parallax2.jpg"
               style="border-radius: 20px"
               height="200px">
          >
          <div class="absolute-bottom text-subtitle2 text-center">
            Title
          </div>
        </q-img>
      </div>

      <div class="row q-pa-sm">
        <q-img src="https://cdn.quasar.dev/img/parallax2.jpg"
               style="border-radius: 20px"
               height="200px">
          >
          <div class="absolute-bottom text-subtitle2 text-center">
            Title
          </div>
        </q-img>
      </div>

    </div>


  </div>
</template>

<script>
export default {
  name: "HomeBanners",
  data() {
    return {
      slide: 1
    }
  }
}
</script>

<style scoped>

</style>
