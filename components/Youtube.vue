<template>
  <div class="is-transparent hero-body is-small" >
      <div class="container has-text-centered">
        <h2 class="is-subtitle">
          Youtube 
        </h2>
        <div class="columns is-centered is-vcentered">
          <div class="column is-8 is-centered">
            <div class="hero is-fullheight">
               <b-carousel-list v-model="test" :data="items" :items-to-show="2">
                  <template slot="item" slot-scope="list">
                      <div class="card" style="background: transparent;">
                        <!-- {{ list.link }} -->
                          <div class="card-image">
                            <iframe width="420" height="315"
                              :src="list.link">
                            </iframe>  
                          </div>
                          <div class="card-content" style="height: 6em;">
                              <div class="content">
                                  <p class="subtitle is-5">{{ list.title }}</p>
                              </div>
                          </div>
                      </div>
                  </template>
              </b-carousel-list>
                     
            </div>
          </div>
        </div>
      </div>
  </div>
</template>
<script>
import Card from '~/components/Card'
import NuxtSSRScreenSize from 'nuxt-ssr-screen-size'
export default {
  data() {
    return {
      test: 0,
      items: [
        {
            title: 'chat with David Deutsch about The Beginning of Infinity',
            link: 'https://www.youtube.com/embed/t511rshmw1Y',
        },
        {
            title: 'I recreated myself one step at a time                      ',
            link: 'https://www.youtube.com/embed/G1oVhF7gBgE',
        },
        {
            title: 'we can always get better at making friends                 ',
            link: 'https://www.youtube.com/embed/HhtvLR1kmJ0',
        },
        {
            title: 'Be prolific. Diagnose and resolve your childhood issues. Escape Jailworld',
            link: 'https://www.youtube.com/embed/cisTub8eJCg'
        },
        {
            title: 'doing anything substantial requires project management',
            link: 'https://www.youtube.com/embed/XdrD9FkBs80',
        },
        {
            title: 'masculinity is about using your strength to nourish others',
            link: 'https://www.youtube.com/embed/RRcPqW9yAs4',
        },
        {
            title: 'project management II: partitioning and celebrating your wins',
            link: 'https://www.youtube.com/embed/lZe5kXpPsJc',
        },
        {
            title: 'my theory of happiness                        ',
            link: 'https://www.youtube.com/embed/BJ2llC5tRXY',
        }
      ]
      }
    },
    methods: {
      info(value) {
          this.test = value
      }
    },
    components: {
      Card,
    },
    mixins: [NuxtSSRScreenSize.NuxtSSRScreenSizeMixin],  
    // methods: {
    //   getWidth () {
    //     return this.$vssWidth
    //   }
    // },

};
</script>
<style scoped lang='scss'>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@1,500&display=swap');
.card {
    display:flex;
    flex-direction: column;
}
.is-subtitle { 
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  font-family: 'Montserrat', sans-serif;  /* padding-bottom: 5px; */
  margin-bottom: 1em;
}
</style>
