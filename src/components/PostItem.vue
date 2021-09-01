<template>
  <div class="post">
      <div>
        <div><strong>Название поста: {{ post.title }}</strong></div>
        <div><strong>Описание поста: {{ post.body }}</strong></div>
      </div>
      <div class="post__btns">
        <my-button
          @click="$emit('remove', post)"
        >
          Удалить пост
        </my-button>
      </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.post {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px;
  margin-top: 15px;
  border: 2px solid teal;
}
</style>