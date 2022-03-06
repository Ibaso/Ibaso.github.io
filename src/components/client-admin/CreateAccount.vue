<template>
  <div>
    <div class="mobile-hide desktop-only">
      <div align="center" class="text-h4 q-pt-xl">
        Create New Customer Account
      </div>

      <div class="row">
        <div class="col-6">
          <div class="row">
            <div class="col-5"></div>
            <div class="col-7  q-pa-md">
              <q-card bordered flat square class=" q-pa-md text-grey-10">

                <q-card-section>
                  <div class="text-h6 text-black">
                    Personal Information
                  </div>
                  <br>
                  <label>First Name</label>
                  <q-input :rules="[val => !!val || 'Field is required']" standout outlined v-model="firstName"/>
                  <br>
                  <label>Last Name</label>
                  <q-input :rules="[val => !!val || 'Field is required']" outlined v-model="lastName"/>
                  <q-option-group
                    size="xs"
                    :options="options"
                    type="checkbox"
                    v-model="group"
                  />
                  ?
                </q-card-section>
                <q-card-actions>
                  <q-btn class="q-mt-md" style="width: 100%" color="secondary" label="Back"/>
                </q-card-actions>
              </q-card>
            </div>
          </div>
        </div>
        <div class="col-6">
          <div class="row">
            <div class="col-7 q-pa-md">
              <q-card bordered flat square class=" q-pa-md ">

                <q-card-section>
                  <div class="text-h6 text-black">
                    Sign-in Information
                  </div>
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
                  <br>
                  <label>Confirm Password</label>
                  <br>
                  <q-input :rules="[val => !!val || 'Field is required']" outlined standout v-model="confirmPassword"
                           :type="isPwd ? 'password' : 'text'">
                    <template v-slot:append>
                      <q-icon
                        :name="isPwd ? 'visibility_off' : 'visibility'"
                        class="cursor-pointer"
                        @click="isPwd = !isPwd"
                      />
                    </template>
                  </q-input>
                </q-card-section>
                <q-card-actions>
                  <q-btn class="q-mt-md" style="width: 100%" color="secondary" label="Create An Account"/>
                </q-card-actions>
              </q-card>
            </div>
          </div>
        </div>

      </div>
    </div>
    <div class="mobile-only desktop-hide" >
      <div align="center" class="text-h4 q-pt-xl">
        Create New Customer Account
      </div>
      <div class="q-pa-md" >
        <q-card bordered flat square class=" q-pa-md text-grey-10">

          <q-card-section>
            <div class="text-h6 text-black">
              Personal Information
            </div>
            <br>
            <label>First Name</label>
            <q-input :rules="[val => !!val || 'Field is required']" standout outlined v-model="firstName"/>
            <br>
            <label>Last Name</label>
            <q-input :rules="[val => !!val || 'Field is required']" outlined v-model="lastName"/>
            <q-option-group
              size="xs"
              :options="options"
              type="checkbox"
              v-model="group"
            />
            ?
          </q-card-section>
          <q-card-actions>
            <q-btn class="q-mt-md" style="width: 100%" color="secondary" label="Back"/>
          </q-card-actions>
        </q-card>
      </div>
      <div class="q-pa-md">
        <q-card bordered flat square class=" q-pa-md ">

          <q-card-section>
            <div class="text-h6 text-black">
              Sign-in Information
            </div>
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
            <br>
            <label>Confirm Password</label>
            <br>
            <q-input :rules="[val => !!val || 'Field is required']" outlined standout v-model="confirmPassword"
                     :type="isPwd ? 'password' : 'text'">
              <template v-slot:append>
                <q-icon
                  :name="isPwd ? 'visibility_off' : 'visibility'"
                  class="cursor-pointer"
                  @click="isPwd = !isPwd"
                />
              </template>
            </q-input>
          </q-card-section>
          <q-card-actions>
            <q-btn class="q-mt-md" style="width: 100%" color="secondary" label="Create An Account"/>
          </q-card-actions>
        </q-card>
      </div>
    </div>
    <home-footer/>
  </div>
</template>

<script>
import HomeFooter from "components/home/HomeFooter";

export default {
  name: "CreateAccount",
  components: {HomeFooter},
  data() {
    return {
      group: [],
      options: [
        {
          label: 'Sign Up for Newsletter',
          value: 'signup'
        },
        {
          label: 'Allow remote shopping assistance',
          value: 'allow'
        }
      ],
      firstName: '',
      lastName: '',
      email: '',
      password: '',
      confirmPassword: '',
      isPwd: 'true'
    }
  }
}
</script>

<style scoped>

</style>
