<template>
  <div class="">
    <q-card style="border-radius: 20px" class="box-shadow ">
      <q-card-section horizontal>
      <q-card-section class="col-5" >
        <q-img
          width="130%"
          class="col q-pa-xs"
          src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/b4a559eee0d025702b27a3241d33543d/3/0/x30_1.jpg.pagespeed.ic.S0eGKhfIz5.webp"
        />
      </q-card-section>

        <q-card-section vertical class="justify-around col-7   q-px-md" >
        <span>
          <div class=" no-wrap items-center q-pa-md">
            <div class="row text-blue-12 text-h6 cursor-pointer ">
            Unlocked Galaxy Mobile Phone
            </div>
            <q-rating size="18px" model-value="4" :max="5"   />
            <br><br>
            <div class="text-subtitle1">
              <b>$ 900.00</b>
            </div>
            <div class="text-subtitle1">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci culpa est illo iste minima numquam quas quia tempora veniam voluptas.
            </div>
            <q-linear-progress  size="8px" :value="0.33" rounded color="negative" class="q-mt-sm" />
            <div class="text-subtitle1">
              Sold: 33/100
            </div>
            <q-btn class="q-mt-md" style="width: 100%" rounded color="secondary" label="ADD TO CARD" />
        </div>
        </span>
        </q-card-section>


      </q-card-section>
    </q-card>
  </div>
</template>

<script>
export default {
  name: "FlashDealComponent"
}
</script>

<style scoped>

</style>
