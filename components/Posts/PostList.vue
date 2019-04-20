<template>
  <section class="post-list">
    <PostPreview
      v-for="item in posts"
      :key="item.id"
      :id="item.id"
      :is-admin="isAdmin"
      :thumbnail="item.thumbnail"
      :title="item.title"
      :previewText="item.previewText" />
  </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview'

export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    },
    posts: {
      type: Array,
      require: true
    }
  }
}
</script>


<style scoped>

.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>

