<template>
  <div>

<!--    Desktop Version-->
    <div class="desktop-only mobile-hide">
    <div class="row text-h5 q-pt-xl q-pb-xl">Sed ut perspiciatis unde omnis iste natus error sit voluptatem</div>
    <div class="row">
      <div class="col-2">
        <div class="row">
          <div class="col">Quality</div>
          <div class="col">
            <q-rating :model-value="qValue"/>
          </div>
        </div>
        <div class="row">
          <div class="col">Price</div>
          <div class="col">
            <q-rating :model-value="pValue"/>
          </div>
        </div>
        <div class="row">
          <div class="col">Value</div>
          <div class="col">
            <q-rating :model-value="value"/>
          </div>
        </div>
      </div>
      <div class="col-10 q-pl-xl">{{ content }}
        <br><br>Review by {{ author }}
        <br>Posted on {{ createdDate }}
      </div>

    </div>
  </div>


<!--     Mobile Version-->
    <div class="mobile-only desktop-hide">
      <div class="row text-h5 q-pt-xl q-pb-xl">Sed ut perspiciatis unde omnis iste natus error sit voluptatem</div>


          <div class="row">
            <div class="col-3">Quality</div>
            <div class="col-9">
              <q-rating :model-value="qValue"/>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Price</div>
            <div class="col-9">
              <q-rating :model-value="pValue"/>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Value</div>
            <div class="col-9">
              <q-rating :model-value="value"/>
            </div>
          </div>

        <div class="col-10 q-pt-md">{{ content }}
          <br><br>Review by {{ author }}
          <br>Posted on {{ createdDate }}
        </div>

      </div>
    </div>

</template>

<script>
export default {
  name: "ReviewComponent",
  props: {
    qValue: null,
    pValue: null,
    value: null,
    content: '',
    author: '',
    createdDate: ''
  }
}
</script>

<style scoped>

</style>
