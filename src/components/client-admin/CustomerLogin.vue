<template>
  <div>
    <div>
      <div class="mobile-hide desktop-only">
        <div align="center" class="text-h4 q-pt-xl">
          Customer Login
        </div>

        <div class="row">
          <div class="col-6 q-pr-xl">
            <div class="row">
              <div class="col-5"></div>
              <div class="col-7  q-pa-md">
                <div class="text-h5"><b>Registered Customers</b></div>
                <label class="text-grey-8">If you have an account, sign in with your email address.</label>
                <br>
                <br>
                <label>Email</label>
                <q-input :rules="[val => !!val || 'Field is required']" type="email" standout outlined
                         v-model="email"/>
                <br>
                <label>Password</label>
                <q-input :rules="[val => !!val || 'Field is required']" outlined standout v-model="password"
                         :type="isPwd ? 'password' : 'text'">
                  <template v-slot:append>
                    <q-icon
                      :name="isPwd ? 'visibility_off' : 'visibility'"
                      class="cursor-pointer"
                      @click="isPwd = !isPwd"
                    />
                  </template>
                </q-input>
                <label> Forgot Password? </label>
                <q-btn class="q-mt-md q-pa-md" style="width: 100%" color="secondary" label="Sign In"/>
              </div>
            </div>
          </div>
          <div class="col-6 q-pl-xl">
            <q-separator  vertical/>

            <div class="row">
              <div class="col-7 q-pa-md">
                <div class="text-h5"><b> New Customers </b></div>
                <label class="text-grey-8">Creating an account has many benefits: check out faster, keep more than one address, track orders and more. </label>
                <br>
                <q-btn class="q-mt-md q-pa-md" style="width: 100%" color="secondary" label="Create An Acoount"/>
              </div>
            </div>
          </div>

        </div>
      </div>
      <div class="mobile-only desktop-hide">
        <div class="q-pa-lg">
          <div class="text-h5"><b>Registered Customers</b></div>
          <label class="text-grey-8">If you have an account, sign in with your email address.</label>
          <br>
          <br>
          <label>Email</label>
          <q-input :rules="[val => !!val || 'Field is required']" type="email" standout outlined
                   v-model="email"/>
          <br>
          <label>Password</label>
          <q-input :rules="[val => !!val || 'Field is required']" outlined standout v-model="password"
                   :type="isPwd ? 'password' : 'text'">
            <template v-slot:append>
              <q-icon
                :name="isPwd ? 'visibility_off' : 'visibility'"
                class="cursor-pointer"
                @click="isPwd = !isPwd"
              />
            </template>
          </q-input>
          <label> Forgot Password? </label>
          <q-btn class="q-mt-md q-pa-md" style="width: 100%" color="secondary" label="Sign In"/>
          <br><br><br>
          <div class="text-h5"><b> New Customers </b></div>
          <label class="text-grey-8">Creating an account has many benefits: check out faster, keep more than one address, track orders and more. </label>
          <br>
          <q-btn class="q-mt-md q-pa-md" style="width: 100%" color="secondary" label="Create An Acoount"/>
        </div>

      </div>
      <home-footer/>
    </div>
  </div>
</template>

<script>
  export default {
    name: "CustomerLogin",
    data() {
      return {
        email: '',
        password: '',
      }
    }
  }
</script>

<style scoped>

</style>
