<template>
  <div>
    <q-card style="border-radius: 20px" class="my-card" v-on:mouseenter="isHover = true" v-on:mouseleave="isHover = false" >
      <q-card-section>
        <q-img :src="imageSrc"  >
          <!--                <q-chip  size="md" color="red" text-color="white"   label="New" />-->
        </q-img>
        <q-rating size="18px" v-model="rating" :max="5"   />
      </q-card-section>

      <q-card-section class="q-pt-none">
        <div class="row no-wrap items-center">
          <div class="col text-blue-12 cursor-pointer ">
            {{name}}
          </div>
        </div>
        <div class="text-subtitle1">
          {{price}}$
        </div>
        <q-linear-progress  size="8px" :value="linearValue" rounded color="negative" class="q-mt-sm" />
        <div class="text-subtitle1">
          Sold: {{sold}}/{{max}}
        </div>
      </q-card-section>


    </q-card>
  </div>
</template>

<script>
export default {
  name: "FlashDealMobileComponent",
  props:{
    id:null,
    name:'',
    imageSrc:'',
    rating:null,
    price:null,
    sold : null,
    max: null,

  },

  data (){
    return {
      isHover : false,
      stars : 4,

    }
  },
  computed:{
    linearValue(){
      return this.sold/this.max
    }
  }
}
</script>

<style scoped>

</style>
