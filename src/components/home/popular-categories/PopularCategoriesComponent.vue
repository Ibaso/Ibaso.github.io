<template>
<div>
  <div    class="q-pa-sm col-2">
    <q-card class="my-card" style="border-radius: 20px">

      <q-img style="height: 150px" :src="imageSrc" >
        <div class="absolute-bottom text-subtitle1 text-center">
          {{caption}}
        </div>
      </q-img>
    </q-card>
  </div>
</div>
</template>

<script>
export default {
  name: "PopularCategoriesComponent",
  props : {
    imageSrc: '',
    caption: '',
  }
}
</script>

<style scoped>

</style>
