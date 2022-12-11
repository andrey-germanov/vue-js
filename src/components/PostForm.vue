<template>
  <form @submit.prevent>
    <h4>Create post</h4>
    <my-input
      v-model="post.title"
      placeholder="type title post"
    />
    <my-input
      v-model="post.description"
      placeholder="type description post"
    />
    <my-button @click="createPost">Create post</my-button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        description: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.title = "";
      this.description = "";
    },
  },
};
</script>

<style lang="css" scoped>

</style>
