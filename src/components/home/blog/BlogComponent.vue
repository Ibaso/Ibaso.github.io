<template>
<div >
  <q-card class="my-card" style="border-radius: 20px; width: 500px">
    <q-img  :src="imageSrc" >
                      <q-chip class="q-ma-sm" square size="md" color="secondary" text-color="white"   :label="blogCategory" />
    </q-img>

    <q-card-section>
      <div class="text-subtitle1"><b>{{name}}</b></div>
      <div class="text-subtitle2" style="color:gray">{{shortContent}}...</div>

    </q-card-section>

    <q-card-section class="q-pt-none ">
      <q-separator/>
      <br>
      <div class="row">
        <div class="col" align="left"><label>Read More</label></div>
        <div class="col" align="right"><label>{{createdDate}}</label></div>
      </div>

    </q-card-section>
  </q-card>
</div>
</template>

<script>
export default {
  name: "BlogComponent",
  props:{
    imageSrc:'',
    blogCategory:'',
    name:'',
    shortContent:'',
    createdDate:'',
    
  },

}
</script>

<style scoped>

</style>
