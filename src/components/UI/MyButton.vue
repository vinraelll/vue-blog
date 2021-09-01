<template>
  <button class="button">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'my-button'
}
</script>

<style scoped>
.button {
  padding: 8px;
  font-size: 16px;
  background-color: #fff;
  color: teal;
  border: 1px solid rgb(0, 128, 128);
  cursor: pointer;
  transition: all .3s ease-in;
}

.button:hover {
  color: #fff;
  background-color: #425;
}
</style>