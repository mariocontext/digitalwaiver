<template>

  <header role="banner">

        <nav class="navbar main-navbar" role="navigation" aria-label="main navigation">
            <div class="navbar-brand">

              <div class="navbar-menu" v-bind:class="{ 'is-active': menuActive }">
                <span class="navbar-start">
                  <router-link class="navbar-item" lang="en" to="/eventslist">Events</router-link>
                  <router-link class="navbar-item" lang="en" to="/">Log Out</router-link>
                </span>

              </div>

              <a role="button" class="navbar-burger" v-on:click="toggleMenu" v-bind:class="{ 'is-active': menuActive }" aria-label="menu" aria-expanded="false">
                <div>
                  <span aria-hidden="true"></span>
                  <span aria-hidden="true"></span>
                  <span aria-hidden="true"></span>
                </div>
              </a>

            </div>
        </nav>   
  </header>

</template>



<script>

  
  module.exports = {

    data: function() {
      return {
        menuActive: false
      }
    },
    methods: {
      toggleMenu: function() {
        this.menuActive= !this.menuActive
      }
    }
    
  }

</script>

<style lang="scss" scoped>

.main-navbar a {
  transition: all 0.5s ease;
    &:hover, 
    &:focus {      
      color: #FFF;
      background-color: #FF0100;
  }
}


@media screen and (max-width: 1087px) {
  .navbar-menu.is-active {
    width: 100%;
    background-color: #000;
  }

}

nav .navbar-item.nuxt-link-exact-active {
  color: #FFF;
  &:focus {
  color: #FFF;
  }
}

header {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000;
}

nav {
  font-size: 1.2rem;
  background-color: #000;

  .navbar-brand {
    margin: 0 auto;
    border-bottom:1px solid #a3a3a3;
    @media screen and (min-width: 1088px) {
      border-bottom: 0;
    }
  }

  .navbar-item {
    color: #FF0100;
    height: 5rem;
  }

}


.navbar-burger {
  /* overrides default navbar burger auto calc to right edge */
  margin-left: 0;

  span {
    height: 3px;
  }

}

</style>