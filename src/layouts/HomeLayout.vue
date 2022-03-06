<template>
  <q-layout view="hHh lpR fFf">

    <q-header reveal elevated class="bg-primary text-white" height-hint="98">


      <!--        <div class="row" style="width: 90%; color: white; text-align: center  ">-->
      <!--          &nbsp &nbsp-->
      <!--          <q-select borderless v-model="language" :options="languageOptions"/>-->
      <!--          <q-separator vertical/>-->
      <!--          &nbsp &nbsp-->
      <!--          <q-select borderless v-model="currency" :options="currencyOptions"/>-->
      <!--          <q-separator vertical/>-->
      <!--          &nbsp &nbsp-->

      <!--          <div class=" row no-wrap justify-center items-center content-start">Need Help? &nbsp-->
      <!--            <a class="col" href="tel:+998999998999" style="text-decoration: white; background-color: transparent; color: white ">+998999998999</a>-->

      <!--            <div class=""  >-->
      <!--              <a href="#" style="text-decoration: white; background-color: transparent; color: white ">My Account</a>-->
      <!--            </div>-->

      <!--          </div>-->


      <!--        </div>-->

      <!--      Toolbar only for Desktop-->
      <q-toolbar class="mobile-hide bg-primary text-white  rounded-borders">


        <q-select borderless v-model="language" :options="languageOptions"/>
        <q-separator vertical/>
        &nbsp &nbsp
        <q-select borderless v-model="currency" :options="currencyOptions"/>
        <q-separator vertical/>
        <label> &nbsp Need Help?</label>
        <label> &nbsp +998901234567 </label>

        <q-space/>


        <!--
          notice shrink property since we are placing it
          as child of QToolbar
        -->
        <q-tabs v-model="tab" shrink stretch>
          <q-tab name="tab1" label="My Account"/>
          <q-tab name="tab2" label="About Us"/>
          <q-tab name="tab3" label="Contact Us"/>
          <q-tab name="tab4" label="FAQs"/>
        </q-tabs>
      </q-toolbar>

      <!--      Toolbar only for Desktop-->
      <q-toolbar class="mobile-hide bg-primary text-white justify-between rounded-borders">
        <q-btn size="xl" flat label="Phonix"/>
        <q-space/>

        <q-card class=" row" style="min-width: 500px">
          <q-select
            class="col"
            filled
            bg-color="white"
            v-model="model"
            use-input
            input-debounce="0"
            label="Simple filter"
            :options="options"
            @filter="filterFn"
            style="width: 250px"
            behavior="menu"
          >
            <template v-slot:no-option>
              <q-item>
                <q-item-section class="text-grey">
                  No results
                </q-item-section>
              </q-item>
            </template>
          </q-select>
          <q-input class="col" filled borderless bg-color="white" v-model="text" :dense="dense">
            <template v-slot:append>
              <q-btn round dense flat icon="search"/>
            </template>
          </q-input>
        </q-card>
        &nbsp &nbsp &nbsp &nbsp


        <div style="min-width: 200px" class="q-pl-lg">
          <q-icon size="lg" color="white" name="mdi-account-outline"/>
          <label>Create an Account</label>
        </div>

        <div style="min-width: 125px">
          <q-icon class="cursor-pointer" size="lg" color="white" name="mdi-heart-outline"/>
          <label>My Wish List</label>
        </div>

        <div style="min-width: 125px">
          <q-icon size="lg" color="white" name="mdi-cart-outline"/>
          <label>My Cart</label>
        </div>
      </q-toolbar>
      <q-separator/>
      <div>


        <!--      Toolbar only for Desktop-->
        <q-tabs class="mobile-hide" inline-label align="left">

          <q-tab color="primary" icon="menu" label="Shop by Department">

            <q-menu>
              <q-list dense style="min-width: 100%">
                <q-item clickable v-close-popup>
                  <q-item-section>Open...</q-item-section>
                </q-item>
                <q-item clickable v-close-popup>
                  <q-item-section>New</q-item-section>
                </q-item>
                <q-separator/>
                <q-item clickable>
                  <q-item-section>Preferences</q-item-section>
                  <q-item-section side>
                    <q-icon name="keyboard_arrow_right"/>
                  </q-item-section>

                  <q-menu anchor="top end" self="top start">
                    <q-list>
                      <q-item
                        v-for="n in 3"
                        :key="n"
                        dense
                        clickable
                      >
                        <q-item-section>Submenu Label</q-item-section>
                        <q-item-section side>
                          <q-icon name="keyboard_arrow_right"/>
                        </q-item-section>
                        <q-menu auto-close anchor="top end" self="top start">
                          <q-list>
                            <q-item
                              v-for="n in 3"
                              :key="n"
                              dense
                              clickable
                            >
                              <q-item-section>3rd level Label</q-item-section>
                            </q-item>
                          </q-list>
                        </q-menu>
                      </q-item>
                    </q-list>
                  </q-menu>

                </q-item>
                <q-separator/>
                <q-item clickable v-close-popup>
                  <q-item-section>Quit</q-item-section>
                </q-item>
              </q-list>
            </q-menu>
          </q-tab>
          <q-route-tab to="/page1" label="My Account"/>
          <q-route-tab to="/page2" label="About Us"/>
          <q-route-tab to="/page3" label="Contact Us"/>
          <q-route-tab to="/page4" label="FAQs"/>
        </q-tabs>
      </div>

      <!--      Toolbar for Mobile-->
      <q-toolbar class="desktop-hide mobile-only">
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer"/>

        <q-toolbar-title>

          Phonix
        </q-toolbar-title>
        <q-btn dense flat round icon="shop" @click="toggleRightDrawer"/>
      </q-toolbar>
      <q-toolbar class="desktop-hide mobile-only">
        <q-input class="col" borderless placeholder="Search Entire Store here..." bg-color="white" v-model="text"
                 :dense="dense">
          <template v-slot:prepend>
            <q-icon name=""/>
          </template>
          <template v-slot:append>
            <q-btn round dense flat icon="search"/>
          </template>
        </q-input>
      </q-toolbar>


    </q-header>
    <q-drawer
      v-model="leftDrawerOpen"
      bordered
      behavior="mobile"
      @click="leftDrawerOpen = false"
    >
      <q-scroll-area class="fit">
        <q-toolbar class="GPL__toolbar">
          <q-toolbar-title class="row items-center text-grey-8">

            <span class="q-ml-sm">Phonix</span>
          </q-toolbar-title>
        </q-toolbar>

        <q-list padding>
          <q-item v-for="link in links1" :key="link.text" clickable class="GPL__drawer-item">
            <q-item-section avatar>
              <q-icon :name="link.icon"/>
            </q-item-section>
            <q-item-section>
              <q-item-label>{{ link.text }}</q-item-label>
            </q-item-section>
          </q-item>


        </q-list>
      </q-scroll-area>
    </q-drawer>
    <q-drawer class="desktop-hide mobile-only"  v-model="rightDrawerOpen" side="right" bordered>
      <div class="q-pa-xl" align="center">

        <span>
         <q-icon size="xl" color="blue" name="mdi-basket-off-outline"/><br>
         <label>Your Card is Empty</label>
          <q-btn class="q-mt-md"  rounded color="secondary" label="Return To Shop" @click="toggleRightDrawer" />
        </span>
      </div>
    </q-drawer>
    <q-page-container>
      <router-view/>
    </q-page-container>


        <q-footer elevated class="bg-white text-grey-7 mobile-only">
          <q-toolbar class="justify-around q-pa-sm">
            <div align="center">
              <q-icon class="row" size="md" name="mdi-home-outline" />
              <label class="row" >Home</label>
            </div>
            <div align="center">
              <q-icon class="row" size="md" name="mdi-account-outline" />
              <label class="row" >Account</label>
            </div>
            <div align="center">
              <q-icon class="row" size="md" name="mdi-home" />
              <label class="row" >Home</label>
            </div>
            <div align="center">
              <q-icon class="row" size="md" name="mdi-heart-outline" />
              <label class="row" >Wishlist</label>
            </div>
            <div align="center">
              <q-icon class="row" size="md" name="mdi-cart-outline" />
              <label class="row" >Cart</label>
            </div>


          </q-toolbar>
        </q-footer>

  </q-layout>
</template>

<script>
import {ref} from 'vue'

export default {
  setup: function () {
    const leftDrawerOpen = ref(false)
    const rightDrawerOpen = ref(false)

    return {
      language: "O'zbek",
      languageOptions: ["English", "O'zbek", "Русский"],
      currency: "UZS",
      currencyOptions: ["UZS", "USD", "RUB"],
      leftDrawerOpen,
      rightDrawerOpen,
      tab: ref(''),
      links1: [
        {icon: 'photo', text: 'Home'},
        {icon: 'photo_album', text: 'Shop'},
        {icon: 'book', text: 'Blog'},
        {icon: 'assistant', text: 'Contact Us'},
        {icon: 'people', text: 'About Us'},

      ],

      createMenu: [
        {icon: 'photo_album', text: 'Album'},
        {icon: 'people', text: 'Shared Album'},
        {icon: 'movie', text: 'Movie'},
        {icon: 'library_books', text: 'Animation'},
        {icon: 'dashboard', text: 'Collage'},
        {icon: 'book', text: 'Photo book'}
      ],
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },

      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value
      }
    }
  }

}

</script>
