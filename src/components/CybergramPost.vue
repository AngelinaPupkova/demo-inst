<template>
  <div class="cybergram-post">
    <div class="header level">
      <div class="level-left">
        <figure class="userImage ">
          <img :src="post.userImage"/>
        </figure>
        <span class="username">{{ post.username }}</span>
      </div>
    </div>
    <div class="image-container"
         :class="post.filter"
         :style="{ backgroundImage: 'url(' + post.postImage + ')' }">
    </div>
    <div class='content'>
      <div class="like-container">
      <div class='heart'>
        <i class='far fa-heart fa-lg'
           :class="{'fas': this.post.hasBeenLiked}"
           @click='like'>
        </i>
      </div>
      <p class='likes'>{{post.likes}} likes</p>
      </div>
      <p class='caption'><span>{{post.username}}</span> {{post.caption}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CybergramPost',
  props: {
    post: Object
  },
  methods: {
    like () {
      this.post.likes = this.post.hasBeenLiked ? this.post.likes - 1 : this.post.likes + 1
      this.post.hasBeenLiked = !this.post.hasBeenLiked
    }
  }
}
</script>

<style lang="scss" src='../styles/cybergram-post.scss'>
</style>
