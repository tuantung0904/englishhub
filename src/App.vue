<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'

</script>

<template>
  <div class="page-content">
    <div class="page-content">
      <div class="Page">
        <div class="PageContentWrapper">
          <div class="Navbar">
            <div class="LogoDiv">
              <RouterLink to="/">
                <img class="Logo" src="/src/assets/images/logo-header.png" alt="Logo" />
              </RouterLink>
            </div>

            <div class="NavButtons">
              <nav>
                <RouterLink class="nav-button" to="/">Về TEH</RouterLink>
                <RouterLink class="nav-button" to="/khoa-hoc">Khoá học</RouterLink>
                <RouterLink class="nav-button" to="/trai-nghiem">Trải nghiệm</RouterLink>
                <RouterLink class="nav-button" to="/thu-vien">Thư viện</RouterLink>
                <RouterLink class="nav-button" to="/su-kien">Sự kiện</RouterLink>
                <RouterLink class="nav-button" to="/lien-he">Liên hệ</RouterLink>
              </nav>
            </div>

            <div class="LoginButtonDiv">
              <a href="/login"><button class="nav-button">
                  <p class="ButtonText">Đăng nhập</p>
                </button>
              </a>
            </div>
          </div>


          <div class="PageContent">
            <div class="ContentLeft">
              <RouterView />
            </div>
            <div class="ContentRight">
              <img class="BigLogo" src="/src/assets/images/BigLogo-B8ylSlHo.png" />
              <img class="Sticker Sticker1" src="/src/assets/images/sticker1-B5DMJB1G.png" />
              <img class="Sticker Sticker2" src="/src/assets/images/sticker2-gGfY4Bd0.png" />
              <img class="Sticker Sticker3" src="/src/assets/images/sticker3-yUUXBlou.png" />
            </div>
          </div>



        </div>
      </div>



    </div>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}



.Navbar {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  z-index: 99;
  border-bottom: 2px solid rgba(255, 255, 255, .6)
}

.Navbar .LogoDiv {
  margin: 20px
}

.Navbar .NavButtons {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.Navbar .LoginButtonDiv {
  display: flex;
  justify-content: flex-end;
  align-items: center
}

.Navbar .nav-button {
  padding: 10px 20px;
  margin: 10px;
  background: #ffffff80;
  background: linear-gradient(90deg, #ffffffb3, #fff6);
  border: 1px solid rgba(255, 255, 255, .5);
  border-radius: 10px;
  font-weight: 300;
  font-size: 14px;
  color: #fff
}

.page-content {
  background-image: url('assets/images/BG1-DiVLq7gB.png');
}

@font-face {
  font-family: BDLifelessGrotesk;
  src: url('assets/fonts/BDLifelessGrotesk-SemiBold.otf') format("opentype");
}

* {
  font-family: BDLifelessGrotesk, Arial, Helvetica, sans-serif;
}

html,
body {
  margin: 0;
  max-width: 100vw;
  max-height: 100vh;
  overflow: hidden
}

.Page {
  width: 100vw;
  height: 100vh;
  max-height: 100vh;
  overflow-y: hidden;
  background-position: center center;
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center
}

.PageContentWrapper {
  background: #313cff;
  background: linear-gradient(180deg, #313cff 3%, #0003ca 98%);
  border-radius: 10px;
  width: 90vw;
  height: 90vh;
  padding: 15px;
  box-shadow: 5px 5px 5px #0000008c;
  display: flex;
  flex-direction: column
}

.PageContent {
  flex-grow: 1;
  display: grid;
  grid-template-columns: 1fr 1fr;
  font-family: BDLifelessGrotesk
}

.ContentLeft {
  display: flex;
  flex-direction: column;
  margin-top: 15px;
  padding: 15px 30px;
  background-color: #fff;
  border-radius: 0 0 0 10px;
  border-right: 5px solid #E2AB2D;
  max-height: 100%;
  color: #8e8e8e
}



.ContentRight {
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px
}

.ContentRight .BigLogo {
  max-width: 100%
}

.ContentRight .Sticker {
  position: fixed;
  z-index: 99;
  max-width: 100%;
  max-height: 100%;
  display: block;
  margin: 0 auto
}

.ContentRight .Sticker1 {
  height: 75vh;
  bottom: 0;
  right: 1vw
}

.ContentRight .Sticker2 {
  height: 30vh;
  bottom: 0vh;
  left: 50vw
}

.ContentRight .Sticker3 {
  height: 22vh;
  bottom: 60vh;
  left: 40vw
}
</style>
