<template>
  <div>
    <div class="desktop-only">
      <div>
        <div align="center" class="text-h4 q-pa-xl">
          {{pageHeader}}
        </div>
        <div class="row">
          <div class="col-3 q-pl-xl q-pr-xl">
            <q-card bordered flat>
              <q-list dense class="text-grey-8">
                <q-item v-ripple>
                  <q-item-section>
                    <q-radio v-model="shape" val="myAccount" label="My Account"/>
                  </q-item-section>
                </q-item>

                <q-item v-ripple>
                  <q-item-section>
                    <q-item-label>
                      <q-radio v-model="shape" val="myOrders" label="My Orders"/>
                    </q-item-label>
                  </q-item-section>
                </q-item>

                <q-item v-ripple>
                  <q-item-section>
                    <q-item-label>
                      <q-radio v-model="shape" val="myWishList" label="My Wish List"/>
                    </q-item-label>
                  </q-item-section>
                </q-item>
                <q-item v-ripple>
                  <q-item-section>
                    <q-item-label>
                      <q-radio v-model="shape" val="addressBook" label="Address Book"/>
                    </q-item-label>
                  </q-item-section>
                </q-item>
                <q-item v-ripple>
                  <q-item-section>
                    <q-item-label>
                      <q-radio v-model="shape" val="accountInformation" label="Account Information"/>
                    </q-item-label>
                  </q-item-section>
                </q-item>
                <q-item v-ripple>
                  <q-item-section>
                    <q-item-label>
                      <q-radio v-model="shape" val="storedPaymentMethods" label="Stored Payment Methods"/>
                    </q-item-label>
                  </q-item-section>
                </q-item>
                <q-item v-ripple>
                  <q-item-section>
                    <q-item-label>
                      <q-radio v-model="shape" val="myProductReviews" label="My Product Reviews"/>
                    </q-item-label>
                  </q-item-section>
                </q-item>
                <q-item v-ripple>
                  <q-item-section>
                    <q-item-label>
                      <q-radio v-model="shape" val="newsLetterSubscription" label="Newsletter Subscription"/>
                    </q-item-label>
                  </q-item-section>
                </q-item>
                <q-item v-ripple>
                  <q-item-section>
                    <q-item-label>
                      <q-radio v-model="shape" val="logout" label="Logout"/>
                    </q-item-label>
                  </q-item-section>
                </q-item>
              </q-list>

            </q-card>
          </div>
          <div class="col-9 q-l-xl q-pr-xl">
            <q-tab-panels v-model="shape" animated>
              <q-tab-panel name="myAccount">
                <q-card bordered flat class="">
                  <div class="row q-pa-lg q-pb-xl">

                    <div class="col-6 q-pt-sm">
                      <div class="text-h5">Account Information</div>
                      <div class="text-h6">Contact Information</div>
                      <div class="text-grey-8">
                        <label> John Doe</label><br>
                        <label>example@mail.com</label><br><br>

                        <label @click="shape='accountInformation'"
                               class="q-pr-sm cursor-pointer text-grey-6">Edit</label>
                        <label @click="shape='accountInformation'" class="cursor-pointer text-grey-6">Change
                          Password</label>
                      </div>
                    </div>
                    <div class="col-6 q-pt-sm">
                      <div class="text-h5">&nbsp;</div>
                      <div class="text-h6">Newsletters</div>
                      <div class="text-grey-8">
                        <label> You aren't subscribed to our newsletter.</label><br><br>

                        <label @click="shape='accountInformation'"
                               class="q-pr-sm cursor-pointer text-grey-6">Edit</label>
                      </div>
                    </div>
                  </div>
                </q-card>
                <q-card bordered flat class="q-mt-lg">
                  <div class="row q-pa-lg q-pb-xl">

                    <div class="col-6 q-pt-sm">
                      <div class="text-h5">Address Book</div>

                      <div class="text-h6">Contact Information</div>
                      <div class="text-grey-8">
                        <label> John Doe</label><br>
                        <label>example@mail.com</label><br><br>

                        <label @click="shape='accountInformation'"
                               class="q-pr-sm cursor-pointer text-grey-6">Edit</label>
                        <label @click="shape='accountInformation'" class="cursor-pointer text-grey-6">Change
                          Password</label>
                      </div>
                    </div>
                    <div class="col-6 q-pt-sm">
                      <div class="text-h5">&nbsp;</div>
                      <div class="text-h6">Newsletters</div>
                      <div class="text-grey-8">
                        <label> You aren't subscribed to our newsletter.</label><br><br>

                        <label @click="shape='accountInformation'"
                               class="q-pr-sm cursor-pointer text-grey-6">Edit</label>
                      </div>
                    </div>
                  </div>
                </q-card>
              </q-tab-panel>

              <q-tab-panel name="myOrders">
                <div class="q-pa-sm" style="background: rgb(253,240,213)">
                  <q-icon name="warning" color="warning" size="xs"/>
                  <label class="text-grey-8">You have no items in your wish list.</label>
                </div>
                <q-btn class="q-pa-sm q-ma-sm float-right" rounded style="width: 100px" color="secondary"
                       label="  Back  "/>
              </q-tab-panel>

              <q-tab-panel name="myWishList">
                <div class="text-h6">Movies</div>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </q-tab-panel>
              <q-tab-panel name="addressBook">
                <div class="text-h6">Movies</div>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </q-tab-panel>
              <q-tab-panel name="accountInformation">
                <div class="text-h6">Movies</div>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </q-tab-panel>
              <q-tab-panel name="storedPaymentMethods">
                <div class="text-h6">Movies</div>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </q-tab-panel>
              <q-tab-panel name="myProductReviews">
                <div class="text-h6">Movies</div>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </q-tab-panel>
              <q-tab-panel name="newsLetterSubscription">
                <div class="text-h6">Movies</div>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </q-tab-panel>
              <q-tab-panel name="logout">
                <div class="text-h6">Movies</div>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </q-tab-panel>
            </q-tab-panels>

          </div>
        </div>
      </div>
    </div>
    <div class="mobile-only">
      <div align="center" class="text-h4 q-pa-xl">
        {{pageHeader}}
      </div>
      <q-tab-panels v-model="shape" animated>
        <q-tab-panel name="myAccount">
          <q-card bordered flat class="">
            <div class="row q-pa-lg q-pb-xl">

              <div class="col-6 q-pt-sm">
                <div class="text-h5">Account Information</div>
                <div class="text-h6">Contact Information</div>
                <div class="text-grey-8">
                  <label> John Doe</label><br>
                  <label>example@mail.com</label><br><br>

                  <label @click="shape='accountInformation'"
                         class="q-pr-sm cursor-pointer text-grey-6">Edit</label>
                  <label @click="shape='accountInformation'" class="cursor-pointer text-grey-6">Change
                    Password</label>
                </div>
              </div>
              <div class="col-6 q-pt-sm">
                <div class="text-h5">&nbsp;</div>
                <div class="text-h6">Newsletters</div>
                <div class="text-grey-8">
                  <label> You aren't subscribed to our newsletter.</label><br><br>

                  <label @click="shape='accountInformation'"
                         class="q-pr-sm cursor-pointer text-grey-6">Edit</label>
                </div>
              </div>
            </div>
          </q-card>
          <q-card bordered flat class="q-mt-lg">
            <div class="row q-pa-lg q-pb-xl">

              <div class="col-6 q-pt-sm">
                <div class="text-h5">Address Book</div>

                <div class="text-h6">Contact Information</div>
                <div class="text-grey-8">
                  <label> John Doe</label><br>
                  <label>example@mail.com</label><br><br>

                  <label @click="shape='accountInformation'"
                         class="q-pr-sm cursor-pointer text-grey-6">Edit</label>
                  <label @click="shape='accountInformation'" class="cursor-pointer text-grey-6">Change
                    Password</label>
                </div>
              </div>
              <div class="col-6 q-pt-sm">
                <div class="text-h5">&nbsp;</div>
                <div class="text-h6">Newsletters</div>
                <div class="text-grey-8">
                  <label> You aren't subscribed to our newsletter.</label><br><br>

                  <label @click="shape='accountInformation'"
                         class="q-pr-sm cursor-pointer text-grey-6">Edit</label>
                </div>
              </div>
            </div>
          </q-card>
        </q-tab-panel>

        <q-tab-panel name="myOrders">
          <div class="q-pa-sm" style="background: rgb(253,240,213)">
            <q-icon name="warning" color="warning" size="xs"/>
            <label class="text-grey-8">You have no items in your wish list.</label>
          </div>
          <q-btn class="q-pa-sm q-ma-sm float-right" rounded style="width: 100px" color="secondary"
                 label="  Back  "/>
        </q-tab-panel>

        <q-tab-panel name="myWishList">
          <div class="text-h6">Movies</div>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
        <q-tab-panel name="addressBook">
          <div class="text-h6">Movies</div>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
        <q-tab-panel name="accountInformation">
          <div class="text-h6">Movies</div>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
        <q-tab-panel name="storedPaymentMethods">
          <div class="text-h6">Movies</div>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
        <q-tab-panel name="myProductReviews">
          <div class="text-h6">Movies</div>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
        <q-tab-panel name="newsLetterSubscription">
          <div class="text-h6">Movies</div>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
        <q-tab-panel name="logout">
          <div class="text-h6">Movies</div>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
      </q-tab-panels>
      <div class=" q-pl-md q-pr-md">
        <q-card bordered flat>
          <q-list dense class="text-grey-8">
            <q-item v-ripple>
              <q-item-section>
                <q-radio v-model="shape" val="myAccount" label="My Account"/>
              </q-item-section>
            </q-item>

            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <q-radio v-model="shape" val="myOrders" label="My Orders"/>
                </q-item-label>
              </q-item-section>
            </q-item>

            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <q-radio v-model="shape" val="myWishList" label="My Wish List"/>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <q-radio v-model="shape" val="addressBook" label="Address Book"/>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <q-radio v-model="shape" val="accountInformation" label="Account Information"/>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <q-radio v-model="shape" val="storedPaymentMethods" label="Stored Payment Methods"/>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <q-radio v-model="shape" val="myProductReviews" label="My Product Reviews"/>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <q-radio v-model="shape" val="newsLetterSubscription" label="Newsletter Subscription"/>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <q-radio v-model="shape" val="logout" label="Logout"/>
                </q-item-label>
              </q-item-section>
            </q-item>
          </q-list>

        </q-card>
      </div>

    </div>
    <!--  <home-footer/>-->
  </div>
</template>

<script>
  import HomeFooter from "components/home/HomeFooter";

  export default {
    name: "Admin",
    components: {HomeFooter},
    data() {
      return {
        shape: 'myAccount'
      }
    },
    computed: {
      pageHeader() {
        switch (this.shape) {
          case 'myAccount' :
            return 'My Account'
          case 'myOrders' :
            return 'My Orders'
          case 'myWishList' :
            return 'My WishList'
          case 'addressBook' :
            return 'Address Book'
          case 'accountInformation' :
            return 'Account Information'
          case 'storedPaymentMethods' :
            return 'Stored Payments'
          case 'myProductReviews' :
            return 'My Product Reviews'
          case 'newsLetterSubscription' :
            return 'Newsletter Subscription'
          case 'logout' :
            return 'Logout'

        }
      }
    }
  }
</script>

<style scoped>
  .item :active {
    background: grey;
  }
</style>
