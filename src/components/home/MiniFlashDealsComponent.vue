<template>
  <div>
    <q-card style=" border-radius: 20px" class="box-shadow "  >
      <q-card-section horizontal>
        <q-card-section class="col-5"   >
          <q-img
            width="130%"
            class=" q-pa-xs"
            :src="imageSrc"
          />
        </q-card-section>
        <q-separator />
        <q-card-section  class="justify-around col-7   " >
        <span>
          <div class=" no-wrap items-center ">
            <div class="row text-blue-12 text-subtitle2  cursor-pointer ">
            <b>{{ name }}</b>
            </div>
            <q-rating size="18px" model-value="4" :max="5"/>
            <br><br>
            <div class="text-subtitle1">
              <b> $ {{ price }} .00</b>
            </div>

        </div>
        </span>
        </q-card-section>
      </q-card-section>


    </q-card>
  </div>
</template>

<script>
export default {
  name: "MiniFlashDeals",
  props: {
    id: null,
    name: '',
    imageSrc: '',
    rating: null,
    content: '',
    price: null

  },
}
</script>

<style scoped>

</style>
