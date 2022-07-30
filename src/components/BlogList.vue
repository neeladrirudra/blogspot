<template>
    <div v-for="(post, index) in posts" :key="post.id">
        <h3>{{index}}. {{post.title}}</h3>
        <BlogDetails :content="post.content"/>
    </div>
</template>

<script>
import BlogDetails from '../components/BlogDetails.vue'

const posts = [
    {
        id: 1,
        title: 'Global Recession',
        content: 'abdiufbsdiug87erewjbr',
    },
    {
        id: 2,
        title: 'Russia invades Ukraine',
        content: 'abdiufbsdiug87erewjbr',
    }
];

export default {
  name: 'BlogList',

  data() {
    return {
        posts: [],
    }
  },

  mounted() {
    this.posts = posts;
  },

  components: {
    BlogDetails,
  }
}
</script>

