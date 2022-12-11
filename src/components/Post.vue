<template>
  <div class="post">
    <div>
      <div><strong>Title: </strong>{{ post.title }}</div>
      <div><strong>Decription: </strong>{{ post.description }}</div>
    </div>
    <my-button>Delete</my-button>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      required: true,
      type: Object,
    },
  },
};
</script>

<style lang="css" scoped>
.post {
  padding: 10px;
  border: 1px solid rgb(151, 168, 227);
  margin-top: 10px;
  display: flex;
  justify-content: space-between;
}
</style>
