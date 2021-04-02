<template>
  <div>
    <div id="app">
      <div id="menu" class="header">
        <div class="image"/>
        <router-link to="/">CYBERGRAM</router-link>
        <router-link to="/about">Рандомно</router-link>
        <router-link to="/order">Упорядочено</router-link>
        <form action="" method="post" class="search">
          <div id="search-input">
            <input type="search" name="" placeholder="поиск" class="input"/>
            <img src="https://lh4.googleusercontent.com/-b-5aBxcxarY/UAfFW9lVyjI/AAAAAAAABUg/gQtEXuPuIds/s13/go.png"
                 id="search-input-icon">
          </div>
        </form>
        <router-link to="/SignIn">Вход</router-link>
        <router-link to="/registration">Регистрация</router-link>
      </div>
      <router-view/>
    </div>
    <div class="card">
      <section class="card-box">
        <div class="card--content" v-for="item in Hashtags" :key="item.label">{{ item.label }}</div>
      </section>
    </div>
    <div id="body-app">
      <div class="app-phone">
        <post-body :posts="posts" />
      </div>
    </div>
    <div id="footer">
      <div class="logo left-content"><h1>DEVELOPER2021</h1></div>
      <div class="right-content">
        <router-link class="footerButton right" to="/">О проекте</router-link>
        <router-link class="footerButton right" to="/">помощь</router-link>
        <form action="" method="post" class="emailSub">
          <input type="email" name="" placeholder="Ваш Email" class="emailInput"/>
          <button class="Subscribe">Подписаться</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import PostBody from './components/PostBody'
import posts from './data/posts'

export default {
  name: 'App',
  components: {
    'post-body': PostBody
  },
  data () {
    return {
      posts,
      Hashtags: []
    }
  },
  created () {
    this.generateText()
  },
  methods: {
    generateText: function () {
      for (let i = 0; i < 208; i++) {
        this.Hashtags.push({ label: this.rndStr(8) })
      }
    },
    rndStr (len) {
      let text = '#'
      const chars = 'abcdefghijklmnopqrstuvwxyz'

      for (let i = 0; i < len; i++) {
        text += chars.charAt(Math.floor(Math.random() * chars.length))
      }

      return text
    }
  }
}

</script>

<style lang="scss" src="./styles/app.scss"/>
