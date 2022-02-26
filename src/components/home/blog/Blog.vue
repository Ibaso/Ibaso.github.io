<template>
  <div class="row ">
    <div class="col-11 text-h6">From The Blog</div>

  </div>


  <div class="q-pa-md">
    <q-virtual-scroll
      :items="heavyList"
      virtual-scroll-horizontal

    >
      <template v-slot="{ item, index }">
        <div class="row no-wrap">
          <div style="width: 250px" class="q-pa-sm">

            <blog-component :blog-category="item.blogCategory" :image-src="item.imageSrc" :name="item.name" :short-content="item.shortContent" :created-date="item.createdDate"/>

          </div>
        </div>
      </template>
    </q-virtual-scroll>
  </div>

</template>

<script>
import BlogComponent from "components/home/blog/BlogComponent";
export default {
  name: "Blog",
  components: {BlogComponent},
  data() {
    return {
      position: 0,
      stars: 4,
      isHover: false,
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
  },
}
</script>

<style scoped>

</style>
