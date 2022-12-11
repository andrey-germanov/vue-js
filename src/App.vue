<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  components: {
    PostForm,
    PostList,
  },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "title1",
          description: "description1",
        },
        {
          id: 2,
          title: "title2",
          description: "description2",
        },
        {
          id: 3,
          title: "title3",
          description: "description3",
        },
        {
          id: 4,
          title: "title4",
          description: "description4",
        },
      ],
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  },
};
</script>

<template>
  <div class="wrapper">
    <post-form @create="createPost" />
    <post-list :posts="posts" />
  </div>
</template>

<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>
