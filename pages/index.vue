<template>
  <section class="section px-0 pb-0">
    <div class="hero is-fullheight">
      <div class="columns">
        <div id="index-left-hero" class="column is-5">
          <div class="hero is-fullheight pl-6">
            <div class="hero-body ml-6">
              <div class="columns is-multiline ml-3">
                <div class="column is-full">
                  <p class="has-text-gold is-size-5 is-inline">I AM</p>
                </div>
                <div class="column is-full">
                  <p class="has-text-white extra-spacing is-size-1">TONY PIÑA</p>
                </div>
                <div class="column is-full">
                  <p class="has-text-gold is-size-5">COMPUTER ENGINEER</p>
                </div>
                <div class="column is-full">
                  <p class="has-text-white">
                    I am passionate about computers, coding, cybersecurity, and other topics related to computer science.
                  </p>
                </div>
                <div class="column mt-5">
                  <b-button type="is-gold" outlined>About me</b-button>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="index-right-hero" class="column is-7">
          <img src="~img/profileImage.jpeg" alt="ProfilePhoto">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'IndexPage',
  components: {
    Card
  }
}
</script>
