<template>
  <div>
    <!--   Desktop Version-->
    <div class="mobile-hide" style="background-color: rgb(31,32,36)">
      <div class="row justify-between ">
        <q-card style="background-color: transparent">
          <q-card-section horizontal>
            <q-card-section>
              <q-icon name="local_shipping" color="secondary" size="65px"/>
            </q-card-section>
            <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
            </q-card-section>
          </q-card-section>
        </q-card>
        <q-card style="background-color: transparent">
          <q-card-section horizontal>
            <q-card-section>
              <q-icon name="credit_card" color="secondary" size="65px"/>
            </q-card-section>
            <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
            </q-card-section>
          </q-card-section>
        </q-card>
        <q-card style="background-color: transparent">
          <q-card-section horizontal>
            <q-card-section>
              <q-icon name="question_answer" color="secondary" size="65px"/>
            </q-card-section>
            <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
            </q-card-section>
          </q-card-section>
        </q-card>
        <q-card style="background-color: transparent">
          <q-card-section horizontal>
            <q-card-section>
              <q-icon name="volunteer_activism" color="secondary" size="65px"/>
            </q-card-section>
            <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
            </q-card-section>
          </q-card-section>
        </q-card>
        <q-card style="background-color: transparent">
          <q-card-section horizontal>
            <q-card-section>
              <q-icon name="recent_actors" color="secondary" size="65px"/>
            </q-card-section>
            <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
            </q-card-section>
          </q-card-section>
        </q-card>
      </div>
      <q-separator dark/>
      <div class="q-pt-xl row">
        <div class="col-3 q-pa-md">
      <span>
      <div class="text-h6 text-white">Download App</div>
      <label class="text-subtitle1" style="color: gray">
        Phonix App is now available on App Store & Google Play.
        Get it now.
      </label>
        <br>
        <br>
        <div class="row">
          <q-btn class="col" size="10px" color="primary" icon="shop" label="Play Market"/>
          <q-btn class="col" size="10px" color="primary" icon="apple" label="App Store"/>
        </div>
        </span>
        </div>

        <div class="col-2 q-pa-md">
          <div class="text-h6 text-white">Help & Customer Care</div>
          <label class="text-subtitle1" style="color: gray">
            New Customers
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            How To Use My Account
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Placing an Order
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Payment Methods
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Problems With Your Order
          </label>
        </div>

        <div class="col-2 q-pa-md">
          <div class="text-h6 text-white">Customer Service</div>
          <label class="text-subtitle1" style="color: gray">
            New Customers
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            How To Use My Account
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Placing an Order
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Payment Methods
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Problems With Your Order
          </label>
        </div>

        <div class="col-2 q-pa-md">
          <div class="text-h6 text-white">My Account</div>
          <label class="text-subtitle1" style="color: gray">
            New Customers
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            How To Use My Account
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Placing an Order
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Payment Methods
          </label>
          <br>
          <label class="text-subtitle1" style="color: gray">
            Problems With Your Order
          </label>
        </div>

        <div class="col-3 q-pa-md">
          <div class="text-h6 text-white">Sign Up To NewsLetters</div>
          <label class="text-subtitle1" style="color: gray">
            Join 60.000+ subscribers and get a new discount coupon
            on every Saturday.
          </label>
          <br>
          <q-input bg-color="white" standout bottom-slots v-model="text" placeholder="Enter Your Email" maxlength="12"
                   :dense="dense">
            <template v-slot:append>
              <q-btn color="secondary">Subscribe</q-btn>
            </template>
          </q-input>
          <br>
          <label class="text-subtitle1" style="color: gray">
            By providing your email address, you agree to our
            Privacy Policy and Terms of Service
          </label>

        </div>

        <br>
        <br>
        <q-separator dark/>
        <br>
        <br>
      </div>
      <div class="row justify-center">

        <label class="text-subtitle1 q-pa-sm" style="color: gray">
          About Us
        </label>
        <q-separator dark vertical/>
        <label class="text-subtitle1  q-pa-sm" style="color: gray">
          Customer
        </label>
        <q-separator dark vertical/>
        <label class="text-subtitle1  q-pa-sm" style="color: gray">
          Service
        </label>
        <q-separator dark vertical/>
        <label class="text-subtitle1  q-pa-sm" style="color: gray">
          Privacy Policy
        </label>
        <q-separator dark vertical/>
        <label class="text-subtitle1  q-pa-sm" style="color: gray">
          Site Map
        </label>
        <q-separator dark vertical/>
        <label class="text-subtitle1  q-pa-sm" style="color: gray">
          Advanced Search
        </label>
        <q-separator dark vertical/>
        <label class="text-subtitle1  q-pa-sm" style="color: gray">
          Contact Us
        </label>
      </div>
    </div>


    <!--   Mobile Version-->
    <div>
      <div class="desktop-hide" style="background-color: rgb(31,32,36)">
        <div class="row justify-center ">
          <div class="row">
            <q-card class="col-6 " align="center" style="background-color: transparent">
              <q-card-section>
                <q-icon name="local_shipping" color="secondary" size="65px"/>
              </q-card-section>
              <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
              </q-card-section>
            </q-card>

            <q-card class="col-6" align="center" style="background-color: transparent">
              <q-card-section>
                <q-icon name="credit_card" color="secondary" size="65px"/>
              </q-card-section>
              <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
              </q-card-section>
            </q-card>
          </div>
          <div class="row">
            <q-card class="col-6" align="center" style="background-color: transparent">
              <q-card-section>
                <q-icon name="question_answer" color="secondary" size="65px"/>
              </q-card-section>
              <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
              </q-card-section>
            </q-card>

            <q-card class="col-6" align="center" style="background-color: transparent">
              <q-card-section>
                <q-icon name="volunteer_activism" color="secondary" size="65px"/>
              </q-card-section>
              <q-card-section>
      <span>
        <div class="text-white">
          Free Delivery
        </div>
        <div style="color:gray">
          For all orders over 120$
        </div>
      </span>
              </q-card-section>
            </q-card>
          </div>
        </div>
        <q-separator dark/>
        <div class="q-pa-md bg-grey-10 text-white">
          <q-list dark padding bordered class="rounded-borders" style="100%">
            <q-expansion-item
              label="Download"
            >
              <q-card class="bg-grey-10">
                <q-card-section>
                  <label class="text-subtitle1" style="color: gray">
                    Phonix App is now available on App Store & Google Play.
                    Get it now.
                  </label>
                  <br>
                  <br>
                  <div class="row">
                    <q-btn class="col" size="10px" color="primary" icon="shop" label="Play Market"/>
                    <q-btn class="col" size="10px" color="primary" icon="apple" label="App Store"/>
                  </div>
                </q-card-section>
              </q-card>
            </q-expansion-item>

            <q-expansion-item
              label="Help & Customers"
            >
              <q-card class="bg-grey-10">
                <q-card-section>
                  <label class="text-subtitle1" style="color: gray">
                    New Customers
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    How To Use My Account
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Placing an Order
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Payment Methods
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Problems With Your Order
                  </label>
                </q-card-section>
              </q-card>
            </q-expansion-item>

            <q-expansion-item
              label="Custom Services"
            >
              <q-card class="bg-grey-10">
                <q-card-section>
                  <label class="text-subtitle1" style="color: gray">
                    Help Center
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Contact Us
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Report Abuse
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Submit a Dispute
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Policies & Rules
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Online Return Policy
                  </label>
                </q-card-section>
              </q-card>
            </q-expansion-item>

            <q-expansion-item
              label="My Account"
            >
              <q-card class="bg-grey-9">
                <q-card-section>
                  <label class="text-subtitle1" style="color: gray">
                    Product Support
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Checkout
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Wishlist
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Custom Link
                  </label>
                  <br>
                  <label class="text-subtitle1" style="color: gray">
                    Redeem Voucher
                  </label>

                </q-card-section>
              </q-card>
            </q-expansion-item>

            <q-expansion-item
              label="Sign Up To Newsletter"
            >
              <q-card class="bg-grey-9">
                <q-card-section>
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quidem, eius reprehenderit eos corrupti
                  commodi magni quaerat ex numquam, dolorum officiis modi facere maiores architecto suscipit iste
                  eveniet doloribus ullam aliquid.
                </q-card-section>
              </q-card>
            </q-expansion-item>
          </q-list>
        </div>



        <div class="q-pt-xl row">





          <br>
          <br>
          <q-separator dark/>
          <br>
          <br>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeFooter"
}
</script>

<style scoped>

</style>
