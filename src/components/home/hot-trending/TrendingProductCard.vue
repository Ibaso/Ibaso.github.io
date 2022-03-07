<template>
<div>
  <q-card   style="border-radius: 20px" class="my-card hover-to-show-link " v-on:mouseenter="isHover = true" v-on:mouseleave="isHover = false" >



    <q-img :src="imageSrc" >
      <!--                <q-chip  size="md" color="red" text-color="white"   label="New" />-->
    </q-img>

    <q-card-section>


      <div class="row no-wrap items-center">
        <div class="col text-blue-12 cursor-pointer ">
          {{content}}
        </div>
        <div class="col-auto text-grey text-caption q-pt-md row no-wrap items-center">
          <q-icon name="place" />
          250 ft
        </div>
      </div>

      <q-rating size="18px" v-model="rating" :max="5"   />
    </q-card-section>

    <q-card-section class="q-pt-none">
      <div class="text-subtitle1">
        {{price}}$
      </div>

    </q-card-section>

    <q-separator v-show="isHover" />

    <q-card-actions class="content-center hover-to-show "   style="transition: 1s" >

      <q-btn flat color="primary" >
        Add to card
      </q-btn>
    </q-card-actions>
  </q-card>
</div>
</template>

<script>

export default {
  name: "TrendingProductCard",
  props:{
    id:null,
    imageSrc:'',
    rating:null,
    content:'',
    price:null

  },

  data (){
    return {
      isHover : false,
      stars : 4
    }
  },
  methods:{

  },
  computed:{

  }
}
</script>

<style scoped>
  .hover-to-show {
    display: none;
    transition: all .2s ease-in-out;
  }

  .hover-to-show-link:hover .hover-to-show {
    display: inline;
    transition: all .2s ease-in-out;
  }
</style>
