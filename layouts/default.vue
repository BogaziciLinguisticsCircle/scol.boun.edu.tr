<template>
  <section>
    <aside>
      <h2>Boğaziçi University</h2>
      <h3>Linguistics Circle</h3>
      <hr>
      <Menu />
    </aside>
    <main>
      <transition name="fade">
        <Nuxt />
      </transition>
    </main>
    <footer>
      Made by Yankı Ekin Yüksel
      <br>
      Source Code Available on <a href="https://github.com/BogaziciLinguisticsCircle/scol.boun.edu.tr" target="_blank">Github</a>
    </footer>
  </section>
</template>

<script type="text/javascript">
import Menu from '~/components/Menu.vue'
export default {
  name: "DefaultLayout",
  components: { Menu }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Fira+Sans&display=swap');
@import url('https://fonts.googleapis.com/css?family=Passions+Conflict&display=swap');

@media (max-width: 512px) {
  main {
    min-width: 256px !important;
  }
}

@media (max-width: 256px) {
  main {
    min-width: 128px !important;
  }
}

html, body {
  background-color: #fafafa;
  font-family: "Fira Sans", sans-serif;
  font-weight: 300;
  font-size: 14px;
  margin: 0;
}
section {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: row wrap;
  height: 100vh;
  & > * {
    padding: 1em;
  }
  aside {
    h2 { 
      background-color: #1d1d1d; 
      color: white; 
      padding: 0 .5em;
      margin: 0 -.25em;
    }
    h3 {
      padding: 0 .5em;
      margin: 0 -.25em 1em;
    }
    hr {
      height: 0px;
      width: 100%;
      margin: 0 -.5em 1.25em;
      padding: 0;
    }
    display: flex;
    flex-flow: column wrap;
    max-height: 130px;
    height: 130px;
  }
  main { 
    flex-shrink: 1;
    flex-basis: 50%;
    padding-bottom: 2em;
    max-width: 512px;
    min-width: 512px;
  }
  footer {
    background-color: #fafafa;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 1em;
    font-size: .5em;
    text-align: right;
  }
}

.nuxt-content {
  // p { white-space: break-spaces !important; }
  ul { padding-left: 1em; }
  ul li a { text-decoration: none; color: black; text-decoration: underline; }
}
// PAGE TRANSITIONS
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
