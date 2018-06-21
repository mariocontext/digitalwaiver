<template>
  <span>
    <div class="logo fx">
        <svg enable-background="new 0 0 101.835 60.832" height="100%" id="Layer_1" version="1.1" viewBox="0 0 101.835 60.832" width="100%" x="0px" xml:space="preserve" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg" y="0px">
                                    <polygon fill="#010101" points="101.835,0 77.666,0 70.115,11.786 62.537,0 38.51,0 38.514,0.006 0,0.006 0,60.822 21.19,60.822 
                                    21.19,41.039 44.475,41.039 44.475,24.477 21.19,24.477 21.19,17.141 49.534,17.141 58.125,30.499 38.692,60.832 62.619,60.832 
                                    70.135,49.172 77.634,60.832 101.645,60.832 82.159,30.521 "></polygon>
                                </svg>
    </div>
      <h1 class="has-text-centered">Digital Waiver</h1>

      <section class="login-section">
        <h2>Login</h2>

        <b-field label="Password">
            <b-input type="password" value="" maxlength="30"></b-input>
        </b-field>
        
        <router-link class="login-btn button is-large is-outlined" lang="en" to="/eventslist">Login</router-link>
    </section>

    <footer><sub>TM & ©2018 FX Networks, LLC. All Rights Reserved.</sub></footer>

  </span>
</template>

<script>

export default {

    layout: 'nocontrols'

}

</script>

<style lang="scss" scoped>

.login-section {
  width: 80vw;
  margin: 0 auto;
  @media screen and (min-width: 960px) {
    width: 600px;
  }
}

.login-btn {
  display: block;
  margin: 0 auto;
  width: 50vw;

  @media screen and (min-width: 960px) {
    width: 300px;
  }

}

footer {
  margin-top: 3rem;
  text-align: center;
}
  
</style>
