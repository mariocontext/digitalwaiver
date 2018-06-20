<template>
<!-- each component needs a single containing element and thus using span -->
  <span>

    <div class="main-content container is-fluid">
      <main class="columns is-variable is-5">

        <section class="column general-content">
          <nuxt/>
        </section>

      </main>
    </div>

    <footer>TM & ©2018 FX Networks, LLC. All Rights Reserved.</footer>
    
</span>

</template>

<script>
  
import AppHeader from '../components/general/AppHeader.vue'
import AppFooter from '../components/general/AppFooter.vue'
  
export default {
  
  components: {
    AppHeader,
    AppFooter
  }
  
}
  
</script>


<style scoped>


</style>