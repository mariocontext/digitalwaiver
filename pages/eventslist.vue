<template>
  <span>
      <h1 class="has-text-centered">Events listing</h1>
      <section>
        <ul>
          <li><router-link to="/event">Some Event A</router-link></li>
          <li><router-link to="/event">Some Event B</router-link></li>
          <li><router-link to="/event">Some Event C</router-link></li>
        </ul>

        <div class="designer-notes">Design note: If only one event exists, this list is not shown and the user goes directly to the event page.</div>

      </section>
  </span>
</template>

<script>

</script>

<style lang="scss" scoped>

li {
    font-size: 1.2rem;
    line-height:3rem;
    transition: all 0.5s ease;
    border-bottom: 1px solid #4a4a4a;       
    padding: 0 .5rem;  
}

li:first-child {
    border-top: 1px solid #4a4a4a;
}

li:hover {
    background-color: #FF0100;
}

li:hover > a {
    color:#FFF;
}

</style>
