<template>
  <!-- <nav class="navbar" role="navigation" aria-label="main navigation">
    <img class="logo" src="@/static/logo.png" alt />
    <h4>freeCodeCamp - SLC</h4>
  </nav>-->
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="/">
        <img src="@/static/logo.png" width="40" height="50" />
      </a>

      <a
        role="button"
        class="navbar-burger burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu">
      <div class="navbar-start">
        <nuxt-link to="/" class="navbar-item">Home</nuxt-link>

        <a href="https://www.meetup.com/UtahJS/events/calendar/" class="navbar-item">Calendar</a>
      </div>

      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a href="https://fccslc.netlify.com/" class="button is-secondary">
              <strong>Sign In</strong>
            </a>
            <a href="https://www.freecodecamp.org/" class="button is-primary">
              <strong>Start Learning</strong>
            </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
// import * as logoImage from "@/static/logo.png";
export default {};
</script>

<style>
.navbar {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
img.logo {
  max-height: 70px;
  width: auto;
}
.navbar h4 {
  margin-left: 10px;
}
</style>