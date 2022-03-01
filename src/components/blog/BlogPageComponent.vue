<template>
  <div>
  <div class="desktop-only mobile-hide">
    <div class="q-pt-md q-pl-xl">
      <q-breadcrumbs class="text-grey" active-color="purple">
        <template v-slot:separator>
          <q-icon
            size="1.2em"
            name="arrow_forward"
            color="grey"
          />
        </template>

        <q-breadcrumbs-el label="Home"/>
        <q-breadcrumbs-el label="Blogs"/>

      </q-breadcrumbs>
    </div>

    <div class="row">
      <div class="col-10">
      <div>
        <div class="row">
        <div class="col-6" v-for="item in splicedArray">

          <div class=" q-pa-md">
            <news-component style="" :blog-category="item.blogCategory" :image-src="item.imageSrc" :name="item.name"
                            :short-content="item.shortContent" :created-date="item.createdDate"/>
          </div>
        </div>
        </div>

      </div>
        <div class="q-pa-lg flex flex-center">
          <q-pagination
            v-model="page_number"
            :max="paginationMax"
            direction-links
          />
        </div>
      </div>
      <div class="col-2">
        <div class="">
          <q-input square outlined v-model="text" label="Search posts here..."  maxlength="12" :dense="dense">

            <template v-slot:append>
              <q-icon v-if="text !== ''" name="close" @click="text = ''" class="cursor-pointer" />
              <q-icon name="search" />
            </template>

            <template v-slot:hint>
              Field hint
            </template>
          </q-input>
          <br>
          <br>


          <q-list>
            <q-item>
              <q-item-section>
                <div class="text-h6">Categories</div>

              </q-item-section>
            </q-item>
            <q-separator  inset />
            <q-item>
              <q-item-section>
               Phonix
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                Photography
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                Creative
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                Image
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                Music
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                Travel
              </q-item-section>
            </q-item>
            <q-separator  inset />


            <q-item>
              <q-item-section>
                Uncategorized
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                Headphone
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                Tool
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                Cameras
              </q-item-section>
            </q-item>
            <q-separator  inset />
          </q-list>
          <br>


          <q-list>
            <q-item>
              <q-item-section>
                <div class="text-h6">Recent Posts</div>

              </q-item-section>
            </q-item>
            <q-separator  inset />
            <q-item>
              <q-item-section>
                <q-img class="" src="https://mageblueskytech.com/dukamarket/media/magefan_blog/x14.jpg.pagespeed.ic.d0GSvjj8X3.webp" />
                <div class="text-h6 q-pt-sm">
                  Feature To Look For On Camera Phones
                </div>
                <div class="text-grey-9 text-subtitle2 q-pt-sm">
                  11 June 2021
                </div>
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                <q-img class="" src="https://mageblueskytech.com/dukamarket/media/magefan_blog/x14.jpg.pagespeed.ic.d0GSvjj8X3.webp" />
                <div class="text-h6 q-pt-sm">
                  Feature To Look For On Camera Phones
                </div>
                <div class="text-grey-9 text-subtitle2 q-pt-sm">
                  11 June 2021
                </div>
              </q-item-section>
            </q-item>
            <q-separator  inset />
            <q-item>
              <q-item-section>
                <q-img class="" src="https://mageblueskytech.com/dukamarket/media/magefan_blog/x14.jpg.pagespeed.ic.d0GSvjj8X3.webp" />
                <div class="text-h6 q-pt-sm">
                  Feature To Look For On Camera Phones
                </div>
                <div class="text-grey-9 text-subtitle2 q-pt-sm">
                  11 June 2021
                </div>
              </q-item-section>
            </q-item>
            <q-separator  inset />

          </q-list>
          <br>

          <q-list>
            <q-item>
              <q-item-section>
                <div class="text-h6">Archive</div>

              </q-item-section>
            </q-item>
            <q-separator  inset />
            <q-item>
              <q-item-section>
                March 2022
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                February 2022
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                January 2022
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                December 2021
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                October 2021
              </q-item-section>
            </q-item>
            <q-separator  inset />

            <q-item>
              <q-item-section>
                September 2021
              </q-item-section>
            </q-item>
            <q-separator  inset />

          </q-list>
          <br>

          <q-item>
            <q-item-section>
              <div class="text-h6">Tags</div>

            </q-item-section>
          </q-item>
          <q-separator  inset />
          <q-card flat>
            <q-card-section>
              <q-chip clickable    >
                iphone
              </q-chip>
              <q-chip clickable    >
                android
              </q-chip>
              <q-chip clickable   >
                smart
              </q-chip>
              <q-chip clickable    >
                samsung
              </q-chip>
              <q-chip clickable   >
                laptop
              </q-chip>
              <q-chip clickable    >
                headphones
              </q-chip>

            </q-card-section>
          </q-card>


        </div>
      </div>
    </div>

  </div>
    <div class="mobile-only desktop-hide">
      <div class="q-pt-md q-pl-md">
        <q-breadcrumbs class="text-grey" active-color="purple">
          <template v-slot:separator>
            <q-icon
              size="1.2em"
              name="arrow_forward"
              color="grey"
            />
          </template>

          <q-breadcrumbs-el label="Home"/>
          <q-breadcrumbs-el label="Blogs"/>

        </q-breadcrumbs>
      </div>
      <div>
        <div class="" v-for="item in splicedArray">
          <div class="row">
            <div class="col q-pa-md">

              <news-component style="" :blog-category="item.blogCategory" :image-src="item.imageSrc" :name="item.name"
                              :short-content="item.shortContent" :created-date="item.createdDate"/>
            </div>
          </div>
        </div>
        <div class="q-pa-lg flex flex-center">
          <q-pagination
            v-model="page_number"
            :max="paginationMax"
            direction-links
          />
        </div>
      </div>
    </div>
    <home-footer/>
  </div>
</template>

<script>
import NewsComponent from "components/blog/NewsComponent";
import BlogComponent from "components/home/blog/BlogComponent";
import HomeFooter from "components/home/HomeFooter";

export default {
  name: "BlogPageComponent",
  components: {HomeFooter, BlogComponent, NewsComponent},
  data() {
    return {
      text:'',
      page_number:1,
      heavyList: [
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x14.jpg.pagespeed.ic.d0GSvjj8X3.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021',

        },
        {
          blogCategory: 'Clothes',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/22.jpg',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Accessories',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x3_122.jpg.pagespeed.ic.qErmrLwC5o.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x4_12.jpg.pagespeed.ic.wJq01Kk2u1.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x6_1.jpg.pagespeed.ic.tCBrMh3-sS.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/2210.jpg',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/2210.jpg',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x6_1.jpg.pagespeed.ic.tCBrMh3-sS.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x3_122.jpg.pagespeed.ic.qErmrLwC5o.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x14.jpg.pagespeed.ic.d0GSvjj8X3.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021',

        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/22.jpg',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x3_122.jpg.pagespeed.ic.qErmrLwC5o.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/22.jpg',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },
        {
          blogCategory: 'Photography',
          id: 1,
          imageSrc: 'https://mageblueskytech.com/dukamarket/media/magefan_blog/x3_122.jpg.pagespeed.ic.qErmrLwC5o.webp',
          name: 'Features To Look For On Camera Phones',
          shortContent: 'Смартфон Apple iPhone 13 Pro Max 128GB, небесно-голубой',
          createdDate: '11 Mar 2021'
        },

      ]
    }
  },
  computed:{
    splicedArray(){
      return this.heavyList.slice((this.page_number - 1) * 6, this.page_number * 6);
    },
    paginationMax(){
      return Math.ceil(this.heavyList.length/6)
    }
    }

}
</script>

<style scoped>

</style>
