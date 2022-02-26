<template>
<div>
  <blog-page-component/>
</div>
</template>

<script>
import Blog from "components/home/blog/Blog";
import BlogPageComponent from "components/blog/BlogPageComponent";
export default {
  name: "BlogPage",
  components: {BlogPageComponent, Blog}
}
</script>

<style scoped>

</style>
