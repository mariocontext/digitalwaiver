<template>
<!-- each component needs a single containing element and thus using span -->
  <span>
    <app-header/>

    <div class="main-content container">
      <main class="columns is-variable is-5">

        <section class="column general-content">
          <nuxt/>
        </section>

      </main>
    </div>
    
</span>

</template>

<script>
  
import AppHeader from '../components/general/AppHeader.vue'
  
export default {
  
  components: {
    AppHeader
  }
  
}
  
</script>


<style scoped>


</style>