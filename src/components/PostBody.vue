<template>
  <div class="postBody">
    <div class='feed'>
      <div class="postContainer">
      <cybergram-post  class="postRED" v-for="post in posts"
                      :post="post"
                      :key="posts.indexOf(post)">
      </cybergram-post>
    </div>
  </div>
  </div>
</template>

<script>
import CybergramPost from './CybergramPost'

export default {
  name: 'PostBody',
  props: {
    posts: Array
  },
  components: {
    'cybergram-post': CybergramPost
  }
}
</script>

<style lang='scss' src='../styles/post-body.scss'>
// Styles from stylesheet
</style>
