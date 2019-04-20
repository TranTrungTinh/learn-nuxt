<template>
  <div class="posts-page">
    <PostList :posts="listData" />
  </div>
</template>

<script>
import PostList from '@/components/Posts/PostList'

export default {
  components: {
    PostList
  },
  data() {
    return {
      listData: [
        {
          id: "1",
          thumbnail: "https://static.pexels.com/photos/270348/pexels-photo-270348.jpeg",
          title: "Hi First!",
          previewText: "This my first post!"
        },
        {
          id: "2",
          thumbnail: "https://static.pexels.com/photos/270348/pexels-photo-270348.jpeg",
          title: "Hi Second!",
          previewText: "This my second post!"
        },
        {
          id: "3",
          thumbnail: "https://static.pexels.com/photos/270348/pexels-photo-270348.jpeg",
          title: "Hi Third!",
          previewText: "This my third post!"
        }
      ]
    }
  }
}
</script>


<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
