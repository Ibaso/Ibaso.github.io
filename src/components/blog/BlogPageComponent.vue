<template>
  <div>
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
        <q-breadcrumbs-el label="Blog"/>

      </q-breadcrumbs>
    </div>

    <div class="row">
      <div class="col-10">

        <div v-for="item in heavyList">

          <div class="col q-pa-md">
            <blog-component :blog-category="item.blogCategory" :image-src="item.imageSrc" :name="item.name"
                            :short-content="item.shortContent" :created-date="item.createdDate"/>
          </div>

        </div>
      </div>
      <div class="col-2">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea id magni odio odit qui rem repudiandae rerum vel
        voluptas voluptatum.
      </div>
    </div>

  </div>
</template>

<script>
import NewsComponent from "components/blog/NewsComponent";
import BlogComponent from "components/home/blog/BlogComponent";

export default {
  name: "BlogPageComponent",
  components: {BlogComponent, NewsComponent},
  data() {
    return {
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


      ]
    }
  }
}
</script>

<style scoped>

</style>
