<template>
  <span>
      <h1>Release Submitted!</h1>

      <section>
        <p>Thanks so much for giving us your release!</p>
        <p>We'll be emailing you a copy for your records to:</p>
        <br/>
        <p class="personal-info">Jack Daniels - someone@somesite.com</p>

        <section class="controls columns">
          <div class="column is-variable">
            <router-link class="button is-outlined secondary-button" to="/eventslist">Back to Events</router-link>
          </div>
          <div class="column is-variable">
            <router-link class="button is-outlined" to="/event">Fresh Release</router-link>
          </div>
        </section>

    </section>

  </span>
</template>

<script>


</script>

<style lang="scss" scoped>

.controls {
  margin-top: 1rem;
  justify-content: space-around;
  display: flex;
  align-items: stretch;
  align-content: center;
}

.personal-info {
  color: #FFF;
  font-weight: 700;
}

</style>
