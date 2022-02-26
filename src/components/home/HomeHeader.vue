<template>
  <div>
    <div class="row" style="width: 100%; background-color: rgb(38,60,151); color: white; text-align: center  ">
      &nbsp &nbsp
      <q-select borderless v-model="language" :options="languageOptions"/>
      <q-separator vertical/>
      &nbsp &nbsp
      <q-select borderless v-model="currency" :options="currencyOptions"/>
      <q-separator vertical/>
      &nbsp &nbsp

        <div class=" col no-wrap justify-center items-center content-start">Need Help? &nbsp
          <a href="tel:+998999998999" style="text-decoration: white; background-color: transparent; color: white ">+998999998999</a>
        </div>

        <div class="col " align="right">
          <a href="#" style="text-decoration: white; background-color: transparent; color: white ">My Account</a>
        </div>


    </div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader",
  data() {
    return {
      language: "O'zbek",
      languageOptions: ["English", "O'zbek", "Русский"],
      currency: "UZS",
      currencyOptions: ["UZS", "USD", "RUB"],
    }
  }
}
</script>

<style scoped>

</style>
