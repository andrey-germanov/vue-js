<template>
    <post v-for="post in posts" :post="post" />
</template>

<script>
import Post from "@/components/Post.vue";

export default {
  components: {
    Post,
  },
  props: {
    posts: {
      required: true,
      type: Array,
    },
  },
};
</script>

<style lang="css" scoped>

</style>
