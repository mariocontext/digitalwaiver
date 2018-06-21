<template>
  <span>
    <h1>Comic-Con 2018</h1>
    <h2 class="title is-5">San Diego, CA</h2>
    <h3 class="title is-6">July 19, 2018 – July 22, 2018</h3>

    <section class="waiver-tease">
      <h2>FX Release</h2>
        <p>Teaser text of release text. Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus molestiae esse pariatur? Rerum nesciunt aperiam quia doloremque placeat repellat, architecto nobis laborum hic voluptate numquam excepturi. Tempore provident placeat numquam....</p>
        <button class="button is-outlined" v-on:click="toggleModal">View More</button>

    </section>

    <section class="waiver-content">

      <div class="modal" v-bind:class="{ 'is-active': modalActive }">
        <div class="modal-background" v-on:click="toggleModal"></div>
        <div class="modal-card">
          <header class="modal-card-head">
            <p class="modal-card-title">FX Release</p>
            <button class="delete" aria-label="close" v-on:click="toggleModal"></button>
          </header>
          <section class="modal-card-body">
            <h1>Release Title goes here</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Distinctio quia laudantium cumque omnis, sunt cum, odio similique error doloremque ullam molestias eaque, beatae accusantium et numquam? Obcaecati vitae perspiciatis quas.</p>
            <p>Itaque maxime molestiae nisi perferendis reprehenderit blanditiis atque impedit officiis, doloremque iusto quos dolore consequatur incidunt sed iste sapiente vitae similique accusamus repellat voluptatem veniam odit nemo? Voluptate, eius officia.</p>
            <h2>Example subsection title</h2>
            <p>Similique, excepturi! Voluptates cumque, architecto provident enim, asperiores tempora porro incidunt vel voluptatem consequuntur, quibusdam nobis laudantium quos laboriosam? <a href="#">Example of a link</a> Tempora quis, possimus id iusto praesentium atque dolorem ratione at nostrum.</p>
            <h2>Example subsection title</h2>
            <p>Iusto consequatur maiores accusantium libero est facere voluptas officia doloribus laboriosam ipsum, laudantium recusandae quibusdam reiciendis <strong>example of bold text</strong> reprehenderit beatae eius numquam necessitatibus explicabo ab ipsam magnam velit? Quas impedit iusto aperiam!</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Distinctio quia laudantium cumque omnis, sunt cum, odio similique error doloremque <em>Example of emphasized text</em> ullam molestias eaque, beatae accusantium et numquam? Obcaecati vitae perspiciatis quas.</p>
            <h3>Smaller subsection title</h3>
            <ul>
              <li>list item</li>
              <li>list item</li>
              <li>list item</li>
              <li>list item</li>
              <li>list item</li>
            </ul>
            <p>Itaque maxime molestiae nisi perferendis reprehenderit blanditiis atque impedit officiis, doloremque iusto quos dolore consequatur incidunt sed iste sapiente vitae similique accusamus repellat voluptatem veniam odit nemo? Voluptate, eius officia.</p>
            <p>Similique, excepturi! Voluptates cumque, architecto provident enim, asperiores tempora porro incidunt vel voluptatem consequuntur, quibusdam nobis laudantium quos laboriosam? Tempora quis, possimus id iusto praesentium atque dolorem ratione at nostrum.</p>
            <p>Iusto consequatur maiores accusantium libero est facere voluptas officia doloribus laboriosam ipsum, laudantium recusandae quibusdam reiciendis reprehenderit beatae eius numquam necessitatibus explicabo ab ipsam magnam velit? Quas impedit iusto aperiam!</p>
          </section>
          <footer class="modal-card-foot">
            <button class="button" v-on:click="toggleModal">Close</button>
          </footer>
        </div>
      </div>

    </section>

    <section cass="waiver-personal-info">
      <form class="waiver-form">
        <b-field label="First name">
          <b-input v-model="firstname" required aria-required="true"></b-input>
          </b-field>
        <b-field label="Last name">
          <b-input v-model="lastname" required aria-required="true"></b-input>
        </b-field>
        <b-field label="Email">
              <b-input type="email"
                  value=""
                  maxlength="30"
                  required 
                  aria-required="true"
                  >
              </b-input>
        </b-field>
        <label class="checkbox">
            <input type="checkbox" checked>
                Subscribe to Newsletter  
        </label>

        <div class="controls columns is-mobile">  
          <div class="column is-variable is-half">
            <input class="button is-outlined secondary-button" value="Cancel" type="reset"/>
          </div>
          <div class="column is-variable is-half">
            <router-link class="button is-outlined" to="submitted">I Agree</router-link>
          </div>
          
        </div>
        
      </form>
    </section>

  </span>
</template>

<script>

module.exports = {

    data: function() {
      return {
        modalActive: false
      }
    },
    methods: {
      toggleModal: function() {
        this.modalActive= !this.modalActive
      },
      toggleAgree: function() {
        this.agreeActive= !this.agreeActive;
      },
      danger: function() {
                this.$snackbar.open({
                    duration: 5000,
                    message: 'We are having a technical problem submitting',
                    type: 'is-danger',
                    position: 'is-bottom',
                    actionText: 'Retry',
                    indefinite: true,
                    queue: false
                })
            }
    }
    
  }

</script>

<style lang="scss" scoped>

.waiver-tease p {
  margin-bottom: 1rem;
}

.waiver-form {
  margin-top: 1rem;
}

.controls {
  margin-top: 2rem;
  text-align: center;
}

</style>
