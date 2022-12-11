<template>
  <button class="button">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "my-button",
};
</script>

<style lang="css" scoped>
.button {
  background-color: transparent;
  border: 1px solid rgb(158, 180, 217);
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
</style>
