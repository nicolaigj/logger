<template>
  <div class="navbar" id="nav">
    <h1 class="logo">Logger</h1>
    <img src="@/assets/menu_icon.svg"
    class="navbar__menu-icon"
    :aria-expanded="menuExpanded"
    aria-controls="menu-list"
    @click="toggleMenu()">
    <div class="navitems">
      <router-link class="navitem" @click="toggleMenu()" :to="{name: 'Home'}">Home</router-link>
      <router-link class="navitem" @click="toggleMenu()" :to="{name: 'About'}">About</router-link>
      <router-link class="navitem" @click="toggleMenu()" :to="{name: 'Login'}">Log in</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoggerMenu',
  data: function () {
    return {
      menuExpanded: false
    }
  },
  methods: {
    toggleMenu: function () {
      this.menuExpanded = !this.menuExpanded
    }
  }
}
</script>

<style scoped>
#nav {
  padding: 0;
}

#nav a {
  font-weight: bold;
  color: var(--grey);
}

#nav a.router-link-exact-active {
  color: var(--orange);
}

.navbar {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-gap: 20px;
  grid-area: content;
  align-items: baseline;
  border-bottom: 3px solid var(--blue);
}

.navitems {
  grid-column: span 1 / -1;
  text-align: end;
  align-self: flex-end;
  padding-top: 30px;
  padding-bottom: 5px;
}

.navitem {
  padding: 0 20px 0 20px;
  text-decoration: none;
}

.logo{
  align-items: start;
  margin: 0 0 0 0;
  padding-top: 30px;
  padding-left: 30px;
}

.navbar__menu-icon {
  width: 30px;
  grid-column: span -1;
  justify-self: end;
  align-self: flex-end;
  padding-top: 30px;
  padding-bottom: 5px;
  padding-right: 20px;
}

[aria-controls="menu-list"]{
  display: none;
}

@media (max-width: 700px){
  [aria-controls="menu-list"]{
  display: block;
  }

  .navitems {
    display: none;
  }

  [aria-expanded="true"] ~ .navitems {
    display: grid;
    grid-template-columns: 1fr;
    grid-column: 1 / -1;
    text-align: center;
    align-self: flex-end;
    padding-top: 0px;
  }
}
</style>
