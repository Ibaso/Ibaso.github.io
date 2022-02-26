<template>
  <div>


    <!--  Desktop Version-->


    <div class="q-pl-xl q-pr-xl desktop-only mobile-hide">
      <div class="q-pa-md">
        <q-breadcrumbs class="text-grey" active-color="purple">
          <template v-slot:separator>
            <q-icon
              size="1.2em"
              name="arrow_forward"
              color="grey"
            />
          </template>

          <q-breadcrumbs-el label="Home"/>
          <q-breadcrumbs-el label="Product Details"/>

        </q-breadcrumbs>


      </div>
      <q-card class="q-pa-lg row ">

        <q-tabs

          v-model="tab"
          vertical
          class="text-teal col-1"
        >
          <q-tab name="1">
            <q-img style="width: 100px"
                   src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/4/14-1_1.jpg"/>
          </q-tab>
          <q-tab name="2">
            <q-img style="width: 100px"
                   src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/5/15-1_1.jpg"/>
          </q-tab>
          <q-tab name="3">
            <q-img style="width: 100px"
                   src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/4/14_1.jpg"/>
          </q-tab>
          <q-tab name="4">
            <q-img style="width: 100px"
                   src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/5/15_1.jpg"/>
          </q-tab>
        </q-tabs>

        <q-carousel
          style="height: 500px"
          class=" col-4"
          v-model="slideModel"
          arrows
          navigation
          infinite
          control-color="grey-5 "
        >

          <q-carousel-slide :name="1"
                            img-src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/4/14-1_1.jpg"/>
          <q-carousel-slide :name="2"
                            img-src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/5/15-1_1.jpg"/>
          <q-carousel-slide :name="3"
                            img-src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/4/14_1.jpg"/>
          <q-carousel-slide :name="4"
                            img-src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/5/15_1.jpg"/>
        </q-carousel>
        <div class="q-pl-md q-pr-md col-7">

          <div class="text-blue-12 text-h6">
            Blue G9 Pro 2020 Battery Unlocked
          </div>

          <div class="row">
            <q-rating class=" q-pr-md" model-value="4"/>
            <q-separator vertical/>
            <label class="q-pl-md q-pr-md"> 3 reviews </label>
            <q-separator vertical/>
            <label class="q-pl-md q-pr-md"> Add Your Review</label>
          </div>
          <div class="row">
            <div class="q-pt-md text-negative text-h6"> $800 <label
              class="text-strike text-subtitle1 text-grey">$950</label></div>
          </div>
          <br>
          <q-separator/>
          <br>
          <div class="row text-blue-grey-9">
            <label class="col-4 ">Availability:</label>
            <label class="col-4 text-blue-6">In stock</label>
          </div>
          <div class="row text-blue-grey-9">
            <label class="col-4 ">SKU:</label>
            <label class="col-4  ">Digital 003</label>
          </div>
          <div class="row text-blue-grey-9 q-pt-sm">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea facilis magnam nam nesciunt obcaecati porro
            quam quidem quisquam sit tempore.
          </div>
          <div class="row q-pt-md">
            <q-input
              dense
              class="col-2 q-pr-sm"
              square
              outlined
              v-model.number="model"
              type="number"

            />
            <div class="col-10">
              <q-btn class=" q-pa-sm" style="width: 100%" color="secondary" label="ADD TO CARD"/>
            </div>
          </div>
          <div class="row">
            <div class="col-5 q-pt-md text-blue-grey-9">
              <q-icon name="mdi-heart-outline"/>
              &nbsp Add To Wish List
              <q-icon class="q-pl-lg" name="mdi-layers-triple-outline"/>
              &nbsp Add To Compare

            </div>
            <div class="col-7 q-pt-md  text-blue-grey-9 " align="right">
              <q-icon name="mdi-share-variant-outline"/>
              &nbsp Share
            </div>
          </div>
          <br>

          <q-separator/>
          <div class="row q-pt-md text-blue-grey-9">
            Categories: Top Selling Products, Cameras & Accessories, Smartphone
          </div>
          <div class=" text-blue-grey-9">
            Brands:
          </div>
        </div>
      </q-card>
      <br><br>
      <q-card class="q-pa-lg row">
        <div class="col-12">
          <q-tabs
            dense
            align="center"
            active-color="secondary"
            indicator-color="secondary"
            v-model="detailsTab"
            narrow-indicator
          >

            <q-tab name="details" label="Details"/>
            <q-tab name="more" label="More"/>
            <q-tab name="reviews" label="Reviews"/>
          </q-tabs>
          <q-separator/>

          <q-tab-panels v-model="detailsTab" >
            <q-tab-panel name="details">
              <p>
                Designed by Hans J. Wegner in 1949 as one of the first models created especially for Carl Hansen & Son, and produced since 1950. The last of a series of chairs wegner designed based on inspiration from antique Chinese armchairs. The gently rounded top together with the back and seat offers a variety of comfortable seating positions,ideal for both long visits to the dining table and relaxed lounging.
              </p>
              <p>
                The standard passage, used since the 1500s.
                A light chair, easy to move around the dining table and about the room. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Lorem ipsum dolor sit amet conse ctetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Sit amet conse ctetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </p>
              <q-img src="https://mageblueskytech.com/dukamarket/media/wysiwyg/xdetail_1.jpg.pagespeed.ic.JU3xpzMcVn.webp"/>
              <div align="center" class="text-h4" >
                Get 30% Daily Cash
              </div>
              <div align="center"  class="text-h4" >
                Back with Membership Card.
              </div>
              <br>
              <div align="center" class="text-blue-grey-9 q-pa-xs">
                A new collection of lounge furniture, occasional tables and a stool by Edward Barber & Jay Osgerby offers a relaxed, contemporary attitude toward
              </div>
              <div align="center" class="text-blue-grey-9 q-pa-xs">
                interior design. The lounge furniture includes four individualized sized sofas, and three complementary ottomans. Available in a range of upholstery fabrics and leathers,
              </div>
              <div align="center" class="text-blue-grey-9 q-pa-xs">
                the lounge furniture is distinguished by stitched seams that reinforce its architectural profile, softened by the curvature of cushions on each face.
              </div>
              <div class="row">
                <q-card  class="col-6 q-pa-md shadow-0">
                  <q-img src="https://mageblueskytech.com/dukamarket/media/wysiwyg/xdetail_new_2.png.pagespeed.ic.5dejIQEHSY.webp" />
                </q-card>
                <q-card class="col-6 q-pa-md shadow-0">
                  <q-img src="https://mageblueskytech.com/dukamarket/media/wysiwyg/xdetail_new_2.png.pagespeed.ic.5dejIQEHSY.webp" />
                </q-card>
              </div>
              <div class="row q-pa-md">
                <q-img src="https://mageblueskytech.com/dukamarket/media/wysiwyg/xdetail_4.png.pagespeed.ic.jSV5D-7wq5.webp" />
              </div>
              <div align="center" >
                <q-img width="350px" src="data:image/webp;base64,UklGRkIJAABXRUJQVlA4TDYJAAAvV8EfEDfFoG0kR96C4vjjvPuyxwFB27Zx26E4f5wXgrZt47ZDcf44L7iRbLuK0OAJS+VvEhJpyN33phMLLLHEar13yrZs4RzJMZJLJK9IFgAILvwAMAFhAgAmBkyEAMFACMGFieBHMBEgwEQIEEL4xw8mAgQIEABCAAgwABACQPhgACYG/gEAMPADAEwABPiDgQEAGAAYmBDJAVds9/8L7PCo7V7bs+9+8Lj/f1op/v89cZgdFuuifaHzKj7Ma3jgFtwJTtGsYl3f7UjwYF2Xs35w+0M5SU47J+n05RH9hwXbVtVmn75M0V4OFMQw8E8Doe7xty4f27wGLdCazccu3xrfTf6q5DydfWUvWqy9V2aT8ypjTzv6VgO897u3OjpbEXRnx1vf9R4AVvd1kPMqXU9/3ooVH75JrdXy9o9WYOtP5L5K1dOuXuDsFHJAU84CvV3kvErU08UfYO1dckT31uKDxeS+ytLTrvPYMp6c0fgtOO/+j6XpaQ+2TSOHNG0besh5laSnP2HdeHJK49fjB3Jd5ehpx1Zk5JgybJ5LrqsUPe3F2+SczvrwUgl6OnPVyqnknKauXDWTXFcJenoFn5KD+gRXyHmVnqfdezCWHNQb2OP+w5/S83Q8DiwnB7X8AMaT8yo7T2+62rX14BY5r7Lz9DK+Iyf1HS6TByo3T49iMjmpyThKHqjcPN2CDkcHAthCHqjcPF2NTnJSnVhNHqjcPAWoRXIvP/7kHbrc8LRiYNhReRkyZGghDRlS2Rj66uXIEQU08uWroRWNIa+ej25va8+ttvbRz18NqWi8fPH42dPHufX02eMXLysaQ0e2P3s8Jve3tjGPn7WPHFqdIDsj2p48GjU87++Hj3r0pG1EZaP927bhw/JeZdjwtm/bHUchJVIMkEQcABASzXx749szBwMea0WWPyjHEWAp1aGopr/3FyAlInFj0Y3TJQ8KygMSHvCUJCMi3rheyAQR0cZOWrS62mGUo3ZdRRTFcUSDxpciMflFyHlEpKD9OZopNoi/VSMmFCZgPDSnRGRGjJWI6MiZyYUwPoO08VuoArPb7l2oHl+67u38YlYBjJ9D7VYP9dyZ+OvIu1OqyMuLrm6+uig3AgAgqB4DPPfxlHeP/FVVksz8bPf91s2Znde3415XhTlt8ukjf7Xovabb2/vnV5wL/aF1nAOuXw5enFFp7pubdJwDqcmnTzysNOORgh3nhGvv8U3YxN+71vwGe84Xu7/prjjjvAId55K7hw73/zZ9AS2Y/nv/4YN3llhDur7t6qKqM34u0HH+tu+8fZ7l2PP7fzXn9P2w/+OZ1ee5RO6Oc2l68EHTkB4cTJcSEY07eXJcFXve03Vv1+uOc+GZSwtzhLTw4pmFNPPj/T8sr0TP0XJ2nFdOfZmvzP7x5akr264vqXDPJ2ceX3s338iv++uNl+ZQpXvuu3xSvpHfwxOnJxNR1Xue/mfzkd+Miwd/0YKtSu9TFO44Tc3v3367kwY/XH1/vcjIr+vejr55RIMg/swHmfm5NvIznpgPhvg0f2ny6SPt2hPzQRK/5tuNu6A9MR8kv3g6P3RQfNnj+cyD32n6/PuKRjHp+fnXIgOg/zQA/0OAAiM+oMKuf+LvmjZ/92G9Hr89rbDrS1X49dBuotfVBV89WL+v7DwdV+LrTfrtqb9riI71Yn1Uvz31d83bjzxZz7fkPJ292sk1mles9mDnnxL0tA/vkHM6h17yQOXnaccWfEWO6Sts8WA7pVL09Eesd2/Phu/Jffntqcd7jKTkvkrS087z2DKRnNHELTjfSc6rND1d/B7Wfk2O6Ot1eN+H/anK09NlPcC5KU7c/JwDepaR+ypVT3/cihUftXyPvLGNPfK82EKpZD2d16vt6fj95I5lLamLHZO/1/Z07J1H7quEPZ0td6PF2i292F+1nD3tHn/z8jG2qhW5XcWOXb7px37Afnv6v3z1f/4lEdj+AItJS5dbApFlfyqEFBshE4U550XVgToVUABJvsjuZQRWJDoFXTENuBQHmGwh0lY+nBEpaSubJFeYKZCWDyRVMRLZUEYDLQEhpUActYwMylLdBBFRUVgcsxKCqBg1aomU7rqCLEQCAFCUMAWkFCUAUnszU9fTSaKEEVEgAJEhMUKIM3vpK2hhJKzeiC7UouFAkiHTMWL1CibMYsuQ6TaIIBcKQBKajYuoEdX02iwabteEHovxPdSzxLXQEyCu5SCTjEsZUAImZY1iSJkgsdoiwYi0gkoQUcS1wJAQhSyWUsBSOIJFkb4rYAKWyBSciOrgUgoGpWGJ1StiCpEYvlAGISVnYQ4EEimhbRWnhYaaSYyIAry2KzZbY8aIzIgUmJCSIch/kGh5C5AZnSOZdYQz1ClFoKP/J6QNh0Qj9xRzwxHNNT3iRHNCNs4TWja5gSVWz9DO1X3R6lvIkuZojQFlkBRpIQcQdpSWVtaaYJRDIyc1JEWwtf5mbI1iDKGYpJgZoektd13zxmjdAqs5mgfGqQFSw0BSBk1i9YkMSvelbmlSmpymSKFuBGmUolJ2MqMJb05o1G9ivDgyAWD6nSFTCAUnJozQ9LxErwmgy6hrRuXn3MiDHpzxr18zaBKrT2i2xdxWgIianBaZNThmZikS2SEBpJIo35eaHrB5z5bmJOBMykCaBJAipgw1pE0INWLNDCObRhgx6sWwxOobKcIA0mizpZSq+UFqIcsJBVIAtXwvGxj/MCQY5ULwyJY7LSYoChEjy3XQ5JZPwlBqp/mBJVbfqENpddQ4IGqK5YBbD+p6o8PNhjlkPN9pBiFi0nIozMxyRmSWAeda4BZirSkSQGCEJvWGW0vS8MAoYCNiLRdN0JPERhJLrN5BnPNYL4JI28s4b5JakySRURUQGSMxbukOUuO+2QopcClTsNDMrEQia0YZ6Dc3NvSbNAVGZL8QQ9LIKZMyhiIyrDAym9lpciFrrM6Lcb2dCw0UjOqPWEqG+kBcqN4wXUjJmJZEuy2VzcZ5PLJDmQCQhkRkZFYAqZlEMUApC3orF0IQ2ccjdaRNxhbWJitEasccjyjvxiNGY1g3WryINS5MhcYjMsd4RIuFKc3tLAaYUQuN0CAjsuOnMmRUNcW45cFRxZSEiEixmKqnUgAQIVVRZYoGQxE=" />
              </div>
              <p>
                Designed by Puik in 1949 as one of the first models created especially for Carl Hansen & Son, and produced since 1950. The last of a series of chairs wegner designed based on inspiration from antique chinese armchairs. The gently rounded top together with the back and seat offers a variety of comfortable seating positions,ideal for both long visits to the dining table and relaxed lounging. A light chair easy to move around the dining table and about the room. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla.
              </p>
              <br>
              <p>
                <b>Section 1.10.32 of "de Finibus Bonorum et Malorum", written by Cicero in 45 BC.</b>
              </p>
              <p>
                Sound of Marshall, unplugs the chords, and takes the show on the road. Weighing in under 7 pounds, the Kilburn is a lightweight piece of vintage styled engineering. Setting the bar as one of the loudest speakers in its class, the Kilburn is a compact, stout-hearted hero with a well-balanced audio which boasts a clear midrange and extended highs for a sound that is both articulate and pronounced. The analogue knobs allow you to fine tune the controls to your personal preferences while the guitar-influenced leather strap enables easy and stylish travel.
              </p>

            </q-tab-panel>
            <q-tab-panel name="more">
               <div class="row">
                  <div class="col-2 q-pa-sm bg-grey-1 ">Dimensions</div>
                  <div class="col-2 q-pa-sm ">7.25 x 1.65 x 10.25 inches</div>
               </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">Weight</div>
                <div class="col-2 q-pa-sm ">145 gr</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">OS</div>
                <div class="col-2 q-pa-sm ">Android 11</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">Battery</div>
                <div class="col-2 q-pa-sm ">1 Lithium Polymer batteries required. (included)</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">Battery</div>
                <div class="col-2 q-pa-sm ">1 Lithium Polymer batteries required. (included)</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">Connectivity Technologies</div>
                <div class="col-2 q-pa-sm ">Bluetooth, Wifi</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">GPS</div>
                <div class="col-2 q-pa-sm ">Yes</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">Other Display Features	</div>
                <div class="col-2 q-pa-sm ">Wireless</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">Form Factor	</div>
                <div class="col-2 q-pa-sm ">Smartphone</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">Date First Available	</div>
                <div class="col-2 q-pa-sm ">November 1, 2023</div>
              </div>
              <div class="row">
                <div class="col-2 q-pa-sm bg-grey-1 ">Color</div>
                <div class="col-2 q-pa-sm ">Black</div>
              </div>
            </q-tab-panel>
            <q-tab-panel name="reviews">
              <div class="text-h6">Reviews</div>
              <div v-for="review in reviews" >
                <review-component :q-value="review.qValue" :p-value="review.pValue" :value="review.value" :content="review.content" :author="review.author" :created-date="review.createdDate" />
                <br>
                <q-separator/>
              </div>

            </q-tab-panel>
          </q-tab-panels>


        </div>
      </q-card>
      <div class="q-pt-xl">
        <div class="row ">
          <div class="col-11 text-h6">Related Products</div>

        </div>


        <div class="q-pa-md">
          <q-virtual-scroll
            style=""
            :items="heavyList"
            virtual-scroll-horizontal

          >
            <template v-slot="{ item, index }">
              <div class="row no-wrap">
                <div style="width: 250px" class="q-pa-sm">

                  <trending-product-card :image-src="item.imageSrc" :rating="item.rating" :content="item.content" :price="item.price"/>

                </div>
              </div>
            </template>
          </q-virtual-scroll>
        </div>


      </div>
      <div class="q-pt-xl">
        <div class="row ">
          <div class="col-11 text-h6">You Might Also Like!</div>

        </div>


        <div class="q-pa-md">
          <q-virtual-scroll
            style=""
            :items="heavyList"
            virtual-scroll-horizontal

          >
            <template v-slot="{ item, index }">
              <div class="row no-wrap">
                <div style="width: 250px" class="q-pa-sm">

                  <trending-product-card :image-src="item.imageSrc" :rating="item.rating" :content="item.content" :price="item.price"/>

                </div>
              </div>
            </template>
          </q-virtual-scroll>
        </div>


      </div>
    </div>



    <!--  Mobile Version-->


    <div class="mobile-only desktop-hide text-blue-grey-9">
      <div class="q-pa-md">
        <q-breadcrumbs class="text-grey" active-color="purple">
          <template v-slot:separator>
            <q-icon
              size="1.2em"
              name="arrow_forward"
              color="grey"
            />
          </template>

          <q-breadcrumbs-el label="Home"/>
          <q-breadcrumbs-el label="Product Details"/>

        </q-breadcrumbs>
      </div>


      <div class=" q-pa-md ">
        <q-card>
          <q-card-section>
            <q-carousel
              class="q-pa-lg"
              v-model="slide"
              arrows
              navigation
              infinite
              control-color="grey-5 "
            >

              <q-carousel-slide :name="1"
                                img-src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/4/14-1_1.jpg"/>
              <q-carousel-slide :name="2"
                                img-src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/5/15-1_1.jpg"/>
              <q-carousel-slide :name="3"
                                img-src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/4/14_1.jpg"/>
              <q-carousel-slide :name="4"
                                img-src="https://mageblueskytech.com/dukamarket/media/catalog/product/cache/374449341643a9dc7b1eb5634b01a040/1/5/15_1.jpg"/>
            </q-carousel>
          </q-card-section>
          <q-card-section>
            <div class="q-pl-md q-pr-md">

              <div class="text-blue-12 text-h6">
                Blue G9 Pro 2020 Battery Unlocked
              </div>
              <q-rating model-value="4"/>
              <br>
              <div class="row">
                <label class="">3 reviews &nbsp &nbsp </label>
                <q-separator vertical/>
                <label> &nbsp &nbsp Add Your Review</label>
              </div>
              <div class="row">
                <div class=" text-negative text-h6 "> $800</div>
                <div class="q-pl-md q-pt-xs text-strike text-subtitle1 text-grey">$950</div>
              </div>
              <br>
              <q-separator/>
              <br>
              <div class="row text-blue-grey-9">
                <label class="col-4 ">Availability:</label>
                <label class="col-4 text-blue-6">In stock</label>
              </div>
              <div class="row text-blue-grey-9">
                <label class="col-4 ">SKU:</label>
                <label class="col-4  ">Digital 003</label>
              </div>
              <div class="row text-blue-grey-9 q-pt-sm">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea facilis magnam nam nesciunt obcaecati porro
                quam quidem quisquam sit tempore.
              </div>
            </div>
          </q-card-section>

          <q-card-section>
            <div class="row q-pl-md">
              <q-input
                dense
                class="col-5 q-pr-sm"
                square
                outlined
                v-model.number="model"
                type="number"

              />
              <div class="col-7">
                <q-btn class=" q-pa-sm" style="width: 100%" color="secondary" label="ADD TO CARD"/>
              </div>
            </div>
            <div class="q-pa-md">
              <q-icon name="mdi-heart-outline"/>
              &nbsp Add To Wish List
            </div>
            <div class="q-pl-md q-pr-md">
              <q-icon name="mdi-share-variant-outline"/>
              &nbsp Share
              <br>
              <br>
              <q-separator/>
            </div>
            <div class="row q-pa-md">
              Categories: Top Selling Products, Cameras & Accessories, Smartphone
            </div>
            <div class="row q-pl-md q-pr-md">
              Brands:
            </div>

          </q-card-section>
        </q-card>
        <br><br>
        <q-card class="q-pa-lg row">
          <q-list bordered class="rounded-borders col-12">
            <q-expansion-item
              expand-separator
              label="Details"

            >
              <q-card>
                <q-card-section>
                  <p>
                    Designed by Hans J. Wegner in 1949 as one of the first models created especially for Carl Hansen & Son, and produced since 1950. The last of a series of chairs wegner designed based on inspiration from antique Chinese armchairs. The gently rounded top together with the back and seat offers a variety of comfortable seating positions,ideal for both long visits to the dining table and relaxed lounging.
                  </p>
                  <p>
                    The standard passage, used since the 1500s.
                    A light chair, easy to move around the dining table and about the room. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Lorem ipsum dolor sit amet conse ctetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Sit amet conse ctetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </p>
                  <q-img src="https://mageblueskytech.com/dukamarket/media/wysiwyg/xdetail_1.jpg.pagespeed.ic.JU3xpzMcVn.webp"/>
                  <div align="center" class="text-h4" >
                    Get 30% Daily Cash
                  </div>
                  <div align="center"  class="text-h4" >
                    Back with Membership Card.
                  </div>
                  <br>
                  <div align="center" class="text-blue-grey-9 q-pa-xs">
                    A new collection of lounge furniture, occasional tables and a stool by Edward Barber & Jay Osgerby offers a relaxed, contemporary attitude toward
                  </div>
                  <div align="center" class="text-blue-grey-9 q-pa-xs">
                    interior design. The lounge furniture includes four individualized sized sofas, and three complementary ottomans. Available in a range of upholstery fabrics and leathers,
                  </div>
                  <div align="center" class="text-blue-grey-9 q-pa-xs">
                    the lounge furniture is distinguished by stitched seams that reinforce its architectural profile, softened by the curvature of cushions on each face.
                  </div>
                  <div class="row">
                    <q-card  class="col-12 q-pa-md shadow-0">
                      <q-img src="https://mageblueskytech.com/dukamarket/media/wysiwyg/xdetail_new_2.png.pagespeed.ic.5dejIQEHSY.webp" />
                    </q-card>
                  </div>
                  <div class="row">
                    <q-card  class="col-12 q-pa-md shadow-0">
                      <q-img src="https://mageblueskytech.com/dukamarket/media/wysiwyg/xdetail_new_2.png.pagespeed.ic.5dejIQEHSY.webp" />
                    </q-card>
                  </div>
                  <div class="row q-pa-md">
                    <q-img src="https://mageblueskytech.com/dukamarket/media/wysiwyg/xdetail_4.png.pagespeed.ic.jSV5D-7wq5.webp" />
                  </div>
                  <div align="center" >
                    <q-img src="data:image/webp;base64,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" />
                  </div>
                  <p>
                    Designed by Puik in 1949 as one of the first models created especially for Carl Hansen & Son, and produced since 1950. The last of a series of chairs wegner designed based on inspiration from antique chinese armchairs. The gently rounded top together with the back and seat offers a variety of comfortable seating positions,ideal for both long visits to the dining table and relaxed lounging. A light chair easy to move around the dining table and about the room. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla.
                  </p>
                  <br>
                  <p>
                    <b>Section 1.10.32 of "de Finibus Bonorum et Malorum", written by Cicero in 45 BC.</b>
                  </p>
                  <p>
                    Sound of Marshall, unplugs the chords, and takes the show on the road. Weighing in under 7 pounds, the Kilburn is a lightweight piece of vintage styled engineering. Setting the bar as one of the loudest speakers in its class, the Kilburn is a compact, stout-hearted hero with a well-balanced audio which boasts a clear midrange and extended highs for a sound that is both articulate and pronounced. The analogue knobs allow you to fine tune the controls to your personal preferences while the guitar-influenced leather strap enables easy and stylish travel.
                  </p>
                </q-card-section>
              </q-card>
            </q-expansion-item>
            <q-separator/>
            <q-expansion-item
              expand-separator
              label="More Information"
            >
              <q-card>
                <q-card-section>
                  <div class="row q-pb-sm">
                   <b> Dimensions :</b> &nbsp
                    7.25 x 1.65 x 10.25 inches
                  </div>
                  <div class="row q-pb-sm">
                    <b>Weight :</b>  &nbsp
                    145 gr
                  </div>
                  <div class="row q-pb-sm">
                    <b>OS:</b> &nbsp
                    Android 11
                  </div>
                  <div class="row q-pb-sm">
                    <b>Battery:</b>  &nbsp
                    1 Lithium Polymer batteries required. (included)
                  </div>

                  <div class="row q-pb-sm">
                    <b>Connectivity Technologies:</b> &nbsp
                     Bluetooth, Wifi
                  </div>
                  <div class="row q-pb-sm">
                    <b>GPS:</b>
                    Yes
                  </div>
                  <div class="row q-pb-sm">
                    <b>Other Display Features:	</b>  &nbsp
                     Wireless
                  </div>
                  <div class="row q-pb-sm">
                    <b>Form Factor:	</b>  &nbsp
                    Smartphone
                  </div>
                  <div class="row q-pb-sm">
                    <b>Date First Available:	</b>  &nbsp
                    November 1, 2023
                  </div>
                  <div class="row q-pb-sm">
                    <b>Color:</b>  &nbsp
                    Black
                  </div>
                </q-card-section>
              </q-card>
            </q-expansion-item>
            <q-separator/>
            <q-expansion-item
              expand-separator
              label="Reviews"
            >
              <q-card>
                <q-card-section>
                  <div class="text-h6">Reviews</div>
                  <div v-for="review in reviews" >
                    <review-component :q-value="review.qValue" :p-value="review.pValue" :value="review.value" :content="review.content" :author="review.author" :created-date="review.createdDate" />
                    <br>
                    <q-separator/>
                  </div>
                </q-card-section>
              </q-card>
            </q-expansion-item>

          </q-list>

        </q-card>
      </div>
    </div>
    <home-footer/>
  </div>
</template>

<script>
import TrendingProductCard from "components/home/hot-trending/TrendingProductCard";
import HomeFooter from "components/home/HomeFooter";
import ReviewComponent from "components/product-detail/ReviewComponent";
export default {
  name: "ProductDetailComponent",
  components: {ReviewComponent, HomeFooter, TrendingProductCard},
  data() {
    return {
      tab: '1',
      slide: 1,
      splitterModel: 20,
      detailsTab: 'details',
      heavyList: [
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },
        {
          id: 1,
          imageSrc: 'data:image/jpeg;base64,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',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },{
          id: 1,
          imageSrc: 'data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBw8PDxANDRAPDw4NDQ0ODQ0NDQ8NDQ4OFREWFhURFRMaHSggGBolGxUVITEhJSorLi8vFyEzOjMsQygvMCsBCgoKDg0OGxAQGDAfHyAtKy0tLS0vNystKy0rLSstKysrKzUtLSstLS0tLS0tLS0tLS0tNy0tLSstLS0tKzEtLf/AABEIAOEA4QMBIgACEQEDEQH/xAAcAAEAAQUBAQAAAAAAAAAAAAAABgIDBAUIAQf/xABOEAACAQIBBgcKCwUFCQAAAAAAAQIDEQQFBhIhMUEHUWFxdLLRExYiNFJTgZGj0hQXJDVUc4KTlKGxMoSSosEjM0JiwhUlQ0RkZXKz8P/EABoBAQADAQEBAAAAAAAAAAAAAAACAwQFAQb/xAAnEQEAAgIBAwMEAwEAAAAAAAAAAQIDETEEEjITIUEUM1FxImHwQv/aAAwDAQACEQMRAD8A+4gAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABos6cpSpQjRpvRnW0nKa2wpRtpNcrbSXOexG508mdM7F5Yw9J6M6i01thBOpNfZjdmL3y4firv8AdqvYfPcv5y4bJyUarfdJLS7lB60nfwpy262nxt2fLa/mtnfgcalHw6dRzVP+0lOMJTf7MVK9td0le13q2lnZWOZQ7rTxCed8lDycR+Gq9g746Hk4j8LV7DDWBp2v4X8c+0tvCLbFVLK/hKcns2uzuJrSOSJtLY98VDyMR+Frdg74qPkYn8LW7DVPSptKT0oSdoztZxe5S7TIsTjFWUJyTDN74qPkYn8LW7Dzvio+RifwlbsMRI9sPRg9WWRPOSiv+Hin+61F+bSNfi+ELJlHVXrSottpd1pTgm1tSbVn6DIsarODIVDG0Z0a0Iy042Ta133a/wD621CcMfBGWfld+NDIv02n6mPjQyL9Mp+qRy/l/Jc8Jiq2Fld9ynZPe4NKUW+WzRgWfKUa/pc6v+NDIv02n+Z78aGRfptP8zk9Qb3P1Gzo4WNknFXsr6r6y7FhnJwhe8VdO/GhkX6bT5za5Izvybi5aGFxdCpPyI1Y6fq2nKccLDyY+o9+Aq6lC9OcXeM4Npxa2Mv+hvr2VfU1+XY4Pl3ApnnWxtOrgMbLSxODUXGo9tWk9V3xtcfKj6iYpjU6loidgAPHoAAAAAAAAAABDs6JXxkYvZGjS/Oc2+qiYkLzn8dX1FH9ahPHyhfhz9wgVpyyhVdS/wDeTtfiUtGP8kYFvJeKpUajjTm5wrRnGSlHR2N6N1yq/wDEfQc7s1YY190jaNWyvfVpO1r33O1lv2I0WQ8wpU60amI0ZQhJS0ZS0oyad7OKSuvSezWdkWjT7Lm9ipSwlCdZvuksPh5VHLbpujByb5btt85fqY+lGXcXXpQm9SpTrU4Vte5Rbvv4iHZ45bnhcIu4yanVajGpfwouTu533OylbibT3HzanpS2JOMoTqN3WxNptrlaevlXGe2j4eRPy++Yxf2dRPdTm7PU04rSX5pFVJ3SfGkQXg8yzOthsVhZycvgtNdylJ3caVSnVtTvxRdN24lK2xIm1CXgx5l+hZjnau8aZCBSmVXLVYeM9PGB8D4VIJZTnbfSjJ8/dan9EiJpEw4VV/vSf1MP/ZVIpGJqxV/jCN593kYl2ECqEDIp0zXTHtnvfSmFMyaVAu0aJtMJhL7jdjxMl8rYcEV6ecGitXdMFU0lx/sdh0OfAODylo5y042/5GT/ACR9/Pl+siIz31+Zdrpp3ir+oAAZl4AAAAAAAAAABCs6X8tX1FH9apNSEZ2O2Mv5NCg3zadS5PHyhfh8gz6zoqRq/BcPJxt4MnF2cmtTu+K91bZqe3VaN5Py/isLNTlKWjpWnFrRu1tVuPnM7PrJVajjJVoJy8Nzi0r3jJuaklv1yf5Efc6+ISpaL0e61Kjk4aKU6jWk27a9i1eo9mfciPZ9ixeGjlPApJ2dlKDWtq9mmlvs1s4m1vIN3rZRU9BU6cle3dViqEKdnvcZyUlzWvzk3zbg6FClB6rQSs9qW65rcrZ116OKdOCVoVIwVFwi3Vva2vbeV9VuNEra5lGN/CS5nZF+BYapCUlOtWjOpXqJNQclSkowhdJ6EU5a2ldzbslYldCXgrmRp4SbcrX8JONr3WtW/Rv1G1hqSXEW0jSu87ZMZFxSMaMitSJoL9xctqR7pAfD+FKD/wBpSlZ2dKKTtqbVSpdX9K9ZFoRJjwo1tLGqnZ3pxqSb3PTqP3PzIrSgdLpqbpDPmtqXtOmZtCieUKRtsHhbnTx49OfkyGDwtyR5Myfe2oZMyfe2olFOnDDw0562/wBiG+T7COfPFI1CFazaUbzYodzzrpx/7df8kfbj4bmpiXVzrjOTu3gGuRalqR9yPlOo3OSd/l9FgjWOI/oABStAAAAAAAAAAAIRnTJPGSSadqFBO256VR2foa9ZNyCZxeO1vq8P+kizH5IX4aXG5Pp1lo1IxnFbFLU48z3GHQzbw8HpRhLSWxucZW5rxNyiuJfqFO2CsmR/z/xQ7C/DJtPSU5QvOKtGb0NNc0tG6MtFaPdQ87pVUaajsSVuIyIssRZXFnqK+mVqRYTK0z0XVIq0izpDSDx8j4SaK+G6e+UJJ8WqpPtI/Qpkm4QmnjEt6hO64r1JW/Q1GCpXZ3OhrvHEuf1VtWmGRgsLckmTMn3tqLeSsDe2oltGlDDw057f8Md8n2GjPmikajllpWZl5Spww8NOet28CO+T7CPZUyi5ycpPW/UlxLkK8qZQc25Set+pLiRHMZiTDFJme6zZSsVZfB/WTzlhJtJfA5K7dtbskvWzoA5y4OJ3zhpv/p/9UTo04XU/dt+5dbD4QAAoWgAAAAAAAAAAEFzhXy6t9Xh/0mTohOcdNLG1Gr+FQw8nz3qLV6izF5IZOGvSKkhY9NLOqR6jwAVplaZaueph4vKRVpFlSPdI9F7SPdIs6R6pB4+Z5+U/lelvlBr1VJdprsnySes3GekdLE6tqjK/pnI0KpPcfQdDv0az/uXJ6q0erMPo+Q6lGNLujcW1qUE1e/LxIwsq5Qc2232JcSIxk3Spp2vr1vlZkVqrYnD/ACm0va3rEey3jMTtNJiqxlYqTNTiJEMkaW0ttueC+V8v0/qP9UTpQ5s4JIqWX6ad/F6j1cas1+h0mfNdR9yf27OLwgABSsAAAAAAAAAAAIZnJ47LouH69UmZC85vHZdFw/XqlmPyQyeLAuLlNxc0s6q57couW8RO0W1zAX463a+9K/EXK1k1o7LftcbMPJVe1RReyp4L593Z6Tb4udoPl1EdvdMFM9uW7ntyTxcuVJlpMqTDxFcr4HulecrbNX80u0xoZIfEb/4dTpzqRnDSbqSd9NR1X2bHxFayxQ817Re6dbB1Nq44jTmZsEzkmWjjkt8RTUyY+IkP+2KPmvaL3SmWWKHmvaL3S36q34Q9CUHyng3FNtEWxkrMm+eeUoTppYeCjK/hOU9JaNt1ktZ84xE5t6yGXPExw0YsMxylvA475fp9GrdVHShzRwLfP1Lo1bqo6XPn807vLr441WAAFSYAAAAAAAAAABCs5/HZdGw/Xqk1ITnP47LouH69Usx+SGThrweA0s70oqx0otceznKgHrWXafE0/SmiTd2jOkpv9mUb25eL1mrtv38e89vu3cW4jp7t7c9TKbnqZJFUmVJlCZUgIXnFidDEzX+W/wDPI1kcdyl/OyDeLlbza68zUYKhOWk7O0ZW9NjpYJ/jEM2T2mZbT4Y+Ms1cc+Mxa0WjBrVDVNdKYtEq8ditI0eI1mVWqGFUZmu0USrgX+fqfRq3VR0sc08DHz9S6NW6qOljiZvOW+nAACpMAAAAAAAAAAAhGdHjsui4fr1SbkHzr8dl0XD9eqWY/JDJw11xcouLmhQruLlFxcCu4uUXFwK7i5RcXAuplSLKZciz14imVaSli5X8ldeZv6mFg8JTtFJ2nrSt/iZo8oeNS5l15klj4pD7fWZ0MU+1GDqflAsqULXI9iSWZXjtItikdS0bqx1tMWa2qYlQyqxizMGSHRxztK+Bf5+pdGrdVHS5zTwL/P1Lo1bqo6WOFm85dLH4wAAqTAAAAAAAAAAAINnZ47LotDr1SckEzu8dfRaHXqlmPyQvw1lxcouLmhSruLlFxcCu4uUXFwK7i5RcXAuJlUZFm56pAR/H+NS5l15kmh4pT+31mRjHeMvmXXmSin4pT+31mdDFxVz+o+UPyutpFcWSnLD2kWxZ2P8Alz482rrGJMyqxiTMGV0caW8C/wA/UujVuqjpY5o4F/n6l0at1UdLnz+f7kurj8YAAVJgAAAAAAAAAAEDzxfy19FodeqTwgGeb+WvotDr1SePlC/DU3Fy3cXNCrS5cXLdxcGly4uW7i4Fy4uW7i4NLlz1SLVz24NNLjH8of8A4rrzJRB/JKf2+syJ42Xyn7C68yUKXySnzT6zOji4o5/U/KI5ZltIti2SDLNXWyM4qZ2Le1XOpG7sGszEmy/VkY02c7JLp44S/gX+fqXRq3VOlzmfgV+fqXR63VOmDg5/OXTx+MAAKkwAAAAAAAAAAD59ns/lv7rR69Q+gnz/AD5jbGKXlYan6bTn2onTlG/DR3Fy3cXLlS5cXLdxcC5cXLdxcC5cXLdxcC5cXLdxcCK5exypYpX81F+1qGyo520auHVKGkpUnKM9K1m73uuTWQ/P2tbFq30eN+futX+liOYHEOLevazd0+SImu2bPh7qyl2UMbpNs01eoWZYm5YnUOlfPEwxY8HaVJFiTPZSLbZjvdsrVNOBT59pdHrdVHTJzRwH09LLkH5GFrSf8q/qdLnGzect1OAAFaYAAAAAAAAAABFs+clTqwhiKUXKeH0lOEVeUqMrNtLe00nzXJSD2J1LyY2+OKV9a2PYz259Hylmvha7c9F0pyd5TotwcnxtbH6UYPeRQ87W9n7pZ3wh2yg1xcnPeRQ89W9n7o7yKPnq3s/dPe+DtlBhcnPeRR89W9n2DvIo+erez90d8HbKDXFyc95FDz1b2fujvIoeerez90d8HbKDXLWKxEaUJVKklGMYuTlJ2ikt75CePMejb+/rc/gL9EYGP4LsDiVo4mpiaqTvouq4RvubjCyb5XdnnfB2y5xy9lP4TiKlfZGbSgm9apxioxvy2V3ytmvpTtvOkPiUyN5ur9/V94fEpkbyKv39X3iVc2ns1254jWXGvWe91XGvWjob4lMjebq/f1feHxKZG83V+/q+8W/Vz+Ffow53dRca9aLc6yW+73Jazoz4lcjebq/f1O03GQuDTJOCkqlLDQnOLvGda9WUXyOTZGepmUoxQiHANmfWw0auU8XB06mJiqeHpyVpxpXu5Nbr6tXIfXzxK2pHpmmdrYAAeAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA//9k=',
          rating: 4,
          content: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          price: 1290
        },


      ],
      reviews: [
        {
          qValue: 4,
          pValue: 4,
          value: 4,
          content: 'Totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem',
          author: 'JohnSon',
          createdDate: '3/21/21'
        },
        {
          qValue: 4,
          pValue: 4,
          value: 4,
          content: 'Totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem',
          author: 'JohnSon',
          createdDate: '3/21/21'
        },
        {
          qValue: 4,
          pValue: 4,
          value: 4,
          content: 'Totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem',
          author: 'JohnSon',
          createdDate: '3/21/21'
        },
      ]
    }
  },
  computed: {
    slideModel() {
      return parseInt(this.tab)
    }
  }

}
</script>

<style scoped>

</style>
