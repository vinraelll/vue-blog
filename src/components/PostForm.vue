<template>
  <form @submit.prevent>
      <h4>Создание нового поста</h4>
      <my-input 
        v-model="post.title"
        placeholder="Название поста"/>
      <my-input 
        v-model="post.body"
        placeholder="Описание поста"/>
      <my-button 
        @click="createPost"
        style="display: block; margin-left: auto; margin: 15px 15px 0 auto;"
      >
        Создать пост
      </my-button>
    </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now()
      this.$emit('create', this.post)
      this.post = {
        title: '',
        body: ''
      }
    },
  },
  watch: {
    post: {
      handler(newVal) {
        console.log(newVal);
      },
      deep: true
    }
  }
}
</script>

<style scoped>

</style>