<template>
  <div class="is-transparent hero-body" >
      <div class="container has-text-centered">
        <h2 class="is-subtitle">
          Twitter 
        </h2>
        <div class="columns is-centered is-vcentered">
          <div class="column is-8 is-centered" style="margin-left: 5em;">
            <div class="hero is-fullheight">
              <a class="twitter-timeline" data-width="800" data-height="800" data-theme="dark" href="https://twitter.com/visakanv?ref_src=twsrc%5Etfw">Tweets by visakanv</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>            </div>
          </div>
        </div>
      </div>
  </div>
</template>
<script>
import Card from '~/components/Card'
import NuxtSSRScreenSize from 'nuxt-ssr-screen-size'

export default {
  async head() {
    return {
      script: [
        {
          src: 'http://platform.twitter.com/widgets.js',
          charset:"utf-8"
        }
      ],
    }
  },
  components: {
    Card,
   },
  mixins: [NuxtSSRScreenSize.NuxtSSRScreenSizeMixin],  
  methods: {
    getWidth () {
      return this.$vssWidth
    }
  },

};
</script>
<style scoped lang='scss'>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@1,500&display=swap');

.is-subtitle { 
  font-weight: 300;
  font-size: 42px;
  color: #f0d353;
  word-spacing: 5px;
  font-family: 'Montserrat', sans-serif;  /* padding-bottom: 5px; */
  margin-bottom: 1em;
}
</style>
