<template>
  <div>
    <div id="app">
      <div id="menu" class="header">
        <div class="image"/>
        <router-link to="/">CYBERGRAM</router-link>
        <router-link to="/about">Рандомно</router-link>
        <router-link to="/order">Упорядочено</router-link>
        <form action="" method="post" class="search">
          <input type="search" name="" placeholder="поиск" class="input"/>
          <input type="submit" name="" value="" class="submit"/>
        </form>
        <router-link to="/SignIn">Вход</router-link>
        <router-link to="/registration">Регистрация</router-link>
      </div>
      <router-view/>
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
    <div class="hashtag">
      <div class="conteiner">
        <ul class="hs">
          <li class="item">test</li>
          <li class="item">test</li>
          <li class="item">test</li>
          <li class="item">test</li>
          <li class="item">test</li>
          <li class="item">test</li>
        </ul>
      </div>
        </div>
      </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap');

body {
  margin: 0;
  max-width: 1200px;
  width: 100%;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 90%;
}

#app {
  background-color: #ffc6ff;
  font-family: 'Roboto', sans-serif;
  text-align: justify;
  display: flex;
}

.image {
  content: url('assets/camera.png');
  width: 50px;
  height: 50px;
  margin: 0;
  margin-left: 10px;
  margin-right: 0;
  padding: 0;
}

#menu {
  a {
    margin: 0;
    left: 70px;
    color: azure;
    display: inline-flex;
    text-decoration: none;

    &:hover {
      color: #000000;
    }
  }
}

/*Header Input*/
.input {
  width: 30%;
  position: relative;
}

.search input {
  border: none;
}

.search .input {
  width: 100%;
  padding: 8px 37px 9px 25px;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.1), inset 0 1px 2px rgba(0, 0, 0, 0.3);
  border-radius: 20px;
  background: #EEE;
  font: 13px 'Roboto', sans-serif;
  color: #555;
  outline: none;
}

.search input:focus {
  box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2), inset 0 1px 2px rgba(0, 0, 0, 0.4);
  background: #E8E8E8;
  color: #333;
}

.search .submit {
  position: absolute;
  display: inline-block;
  top: 18px;
  left: 46%;
  cursor: pointer;
  background: url(https://lh4.googleusercontent.com/-b-5aBxcxarY/UAfFW9lVyjI/AAAAAAAABUg/gQtEXuPuIds/s13/go.png) 50% no-repeat;
  opacity: 0.5;
}

.search .submit:hover {
  opacity: 0.8;
}

input[type="search"] {
  -webkit-appearance: none;
}

/*Footer Input*/
.emailSub {
  width: 20%;
  position: relative;
}

.emailInput {
  border: none;
}

.emailInput {
  padding: 8px 37px 9px 25px;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.1), inset 0 1px 2px rgba(0, 0, 0, 0.3);
  border-radius: 20px;
  background: #EEE;
  font: 13px Tahoma, Arial, sans-serif;
  color: #555;
  outline: none;
  font-family: 'Roboto', sans-serif;
}

.emailInput:focus {
  box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2), inset 0 1px 2px rgba(0, 0, 0, 0.4);
  background: #E8E8E8;
  color: #333;
}

.emailSub .submit:hover {
  opacity: 0.8;
}

input[type="email"] {
  -webkit-appearance: none;
}

button {
  font-family: 'Roboto', sans-serif;
  background-color: #ffc6ff;
  color: #ffffff;
  border-color: #ffc6ff;
  border-radius: 10px;
  border-style: solid;
}

button:before {
  font-family: 'Roboto', sans-serif;
  color: #F9F0DA;
  font-size: 20px;
  font-weight: bold;
  margin-left: 2%;
}

#footer {
  background-color: rgba(218, 218, 218, 0.53);
  font-family: 'Roboto', sans-serif;
  text-align: justify;
  position: absolute;
  max-width: 1200px;
  width: 100%;
  left: 0;
  bottom: 0;
  overflow: hidden;

  .left-content {
    float: left;
    width: 20%;
  }

  .right-content {
    padding: 30px;
    float: right;
  }

  .logo, .footerButton, .emailSub {
    margin-right: 20px;
    color: #020000;
    display: inline-flex;
    padding: 15px;
    margin-left: 10px;
    text-decoration: none;

  }

  .emailSub {
    button {
      margin: 0 0 0 10px;
    }
  }
}

</style>
