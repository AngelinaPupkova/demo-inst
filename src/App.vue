<template>
  <div id="app">
    <div id="menu" class="header">
      <div id="menu" class="image"></div>
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
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap');

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
  content: url('/assets/camera.png');
  width: 50px;
  height: 50px;
  margin: 0;
  padding: 0;
  position: absolute;
  top: 10px;
  left: 10px;
}

#menu {
  padding: 20px;

  a {
    width: 50px;
    margin-left: 40px;
    font-weight: bold;
    color: azure;
    display: inline-flex;
    padding: 15px;
    text-decoration: none;

  }
}

.search {
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
  font: 13px Tahoma, Arial, sans-serif;
  color: #555;
  outline: none;
}

.search .input:focus {
  box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2), inset 0 1px 2px rgba(0, 0, 0, 0.4);
  background: #E8E8E8;
  color: #333;
}

.search .submit {
  position: absolute;
  top: 0;
  right: 0;
  width: 37px;
  height: 100%;
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
</style>
