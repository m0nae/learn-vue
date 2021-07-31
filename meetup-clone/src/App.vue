<template>
  <header>
    <p>MEETUP</p>
    <div>
      <a>LINK</a>
      <a>LINK</a>
      <a>LINK</a>
    </div>
  </header>
  <section id="home-header">
    <h1>Find your next event</h1>
    <h2>111 events in your groups — 398 events near you</h2>
  </section>
</template>

<script setup>
// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md
</script>

<style lang="scss">
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  min-height: 100vh;
  min-width: 100vw;
}

header {
  background-color: #fff;
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 80px;
}

#home-header {
  background-color: rgb(25, 85, 119);
  height: 169px;
  text-align: center;
}
</style>
