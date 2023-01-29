<template>
  <div>
    <nav class="navbar header is-fixed-top cs-shadow is-black px-6" role="navigation" aria-label="main navigation">
      <div class="navbar-brand ml-6">
        <div class="navbar-item">
          <NuxtLink to="/" exact-active-class="is-active">
            TONY PIÑA
          </NuxtLink>
        </div>

        <div class="navbar-burger">
          <span />
          <span />
          <span />
        </div>
      </div>

      <div class="navbar-menu mr-6">
        <div class="navbar-start">
        </div>
        <div class="navbar-end">

          <div v-for="(link, key) of navbar_links" :key="key" class="navbar-link pl-3 py-0">
              <div class="navbar-item">
                  <NuxtLink :to="link.to" exact-active-class="is-active">
                    {{ link.title }}
                  </NuxtLink>
              </div>
          </div>
        </div>
      </div>

    </nav>

    <section class="main-content has-background-black">
      <Nuxt />
    </section>

    <footer class="footer has-background-black p-0">
      <div class="container px-2 pt-6 pb-6">
        <div class="columns is-multiline">
          <div class="column is-2 is-offset-2">
            <p id="title-footer" class="has-text-gold is-size-6 has-text-weight-medium">SITEMAP</p>
            <div class="columns pt-3">
                <ul class="is-size-7 column">
                  <li v-for="(link, link_key) of navbar_links" :key="link_key" class="pl-5">
                    <NuxtLink :to="link.to">
                      <p class="is-size-7 pb-1">{{ link.title }}</p>
                    </NuxtLink> 
                  </li>
                </ul>
            </div>
          </div>
          <div class="column is-4">
            <div class="columns is-multiline">
              <div class="column is-full">
                <div class="columns is-mobile">  
                  <div class="column is-5 is-offset-1 is-flex">
                    <p id="title-footer" class="has-text-weight-semibold">TONY PIÑA</p>
                  </div>
                  <div class="column is-5 is-flex is-justify-content-end">
                    <a href="https://github.com/Tonypina" target="_blank">
                      <span class="ml-5 is-size-5">
                        <fa-icon :icon="faGithub" />
                      </span>
                    </a>
                    <a href="https://www.facebook.com/tony.pina.357/" target="_blank">
                      <span class="ml-5 is-size-5">
                        <fa-icon :icon="faFacebook" />
                      </span>
                    </a>
                    <a href="https://www.instagram.com/pina_rossette" target="_blank">
                      <span class="ml-5 is-size-5">
                        <fa-icon :icon="faInstagram" />
                      </span>
                    </a>
                    <a href="https://whats.jumase.com.mx/" target="_blank">
                      <span class="ml-5 is-size-5">
                        <fa-icon :icon="faWhatsapp" />
                      </span>
                    </a>
                  </div>
                </div>
              </div>
              <div class="column is-10 is-offset-1">
                <p class="has-text-centered has-text-gold">I'll find a creative way to develop your solutions.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div id="copyright" class="hero">
        <div class="hero-body p-0 py-2">
          <p class="has-text-centered is-size-7">© 2023 <span class="has-text-gold">Tony Piña</span>.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
  import { faGithub, faFacebook, faInstagram, faWhatsapp } from '@fortawesome/free-brands-svg-icons'

  export default {
    name: 'DefaultLayout',

    data() {
      return {
        navbar_links: [{
            title: 'HOME',
            to: {
              name: 'index'
            },
          },
          {
            title: 'ABOUT',
            to: {
              name: 'about'
            },
          },
          {
            title: 'PORTFOLIO',
            to: {
              name: 'portfolio'
            },
          },
          {
            title: 'CONTACT',
            to: {
              name: 'contact'
            },
          },
        ],
      }
    },

    computed: {
      faGithub () {
        return faGithub
      },
      
      faFacebook () {
        return faFacebook
      },

      faWhatsapp () {
        return faWhatsapp
      },

      faInstagram () {
        return faInstagram
      }
    },
  }

</script>
