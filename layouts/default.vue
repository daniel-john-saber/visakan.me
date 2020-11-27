<template>
  <div >
    <section id="home" class="hero">
      <div class="hero-head">
        <div class="container has-shadow">
         <!-- mobile nav -->
          <nav class="navbar sandwich-link" role="navigation" aria-label="main navigation">
            <div class="container" style="width: auto;">
                <div class="navbar-brand">
                    <img
                        src="~assets/vv.png"
                        alt="peak"
                        width="150"
                        class="is-pad-left"
                        
                    >
                  <div class="navbar-burger burger" aria-label="menu" data-target="navMenu" aria-expanded="false">
                    <span aria-hidden="true"></span>
                    <span aria-hidden="true"></span>
                    <span aria-hidden="true"></span>
                  </div>
              </div>
              <div class="level navbar-menu" id="navMenu">
                <div class="navbar-end" style="margin-top: 3px">
                  <div class="columns is-mobile">
                    <div class="column">
                      <a class="navbar-item is-tab is-nav-text" href="/">Home</a>
                    </div>
                    <div class="column">
                      <a class="navbar-item is-tab is-nav-text" href="#about">About</a>
                    </div>
                    <div class="column">
                      <a class="navbar-item is-tab is-nav-text" href="#ebook">Ebook</a>
                    </div>
                    <div class="column">
                      <a class="navbar-item is-tab is-nav-text" href="#twitter">Twitter</a>
                    </div>
                    <div class="column">
                      <a class="navbar-item is-tab is-nav-text" href="#youtube">Youtube</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </nav>
        </div>
      </div>
    </section>
    <section id = "background" class="hero is-medium is-default has-background-light-grey">
      <div v-if="getWidth() > 1300">
         <Home/>
      </div>
      <div v-else>
        <MobileHome/>
      </div>

    </section>
    <section id="about" class="hero is-fullheight is-default" style="background: #ECE9E6;  /* fallback for old browsers */
      background: -webkit-linear-gradient(to right, #FFFFFF, #ECE9E6);  /* Chrome 10-25, Safari 5.1-6 */
      background: linear-gradient(to right, #FFFFFF, #ECE9E6); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
      ">
      
      <About/>
    </section>
    <section id="ebook">
      <Ebook/>
    </section>
    <section id="twitter">
      <Twitter/>
    </section>
    <section id="youtube" class="is-small is-default has-background-light-grey" style="height: 40em;">
      <Youtube/>
    </section>
    <footer class="footer">
      <div class="content has-text-centered">
        <p>
          Made with 
          <svg class="icon_made" aria-hidden="true">
            <use xlink:href="#icon-heart-"></use>
          </svg> by <a href="https://danieljohn.me">Daniel John</a>
        </p>
      </div>
    </footer>
    <section class="main-content columns">
      <div class="container column is-10" >
        <!-- <nuxt /> -->
      </div>
    </section> 
  </div>
</template>
<script>

import Home from '~/components/Home'
import MobileHome from '~/components/MobileHome'
import About from '~/components/About'
import Ebook from '~/components/Ebook'
import Twitter from '~/components/Twitter'
import Youtube from '~/components/Youtube'

import NuxtSSRScreenSize from 'nuxt-ssr-screen-size'
import { Icon } from 'ant-design-vue'

const MyIcon = Icon.createFromIconfontCN({
  scriptUrl: '//at.alicdn.com/t/font_2224864_0f2cs090uhai.js', 
})

if (process.browser) {
  document.addEventListener('DOMContentLoaded', () => {

    // Get all "navbar-burger" elements
    const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

    // Check if there are any navbar burgers
    if ($navbarBurgers.length > 0) {

      // Add a click event on each of them
      $navbarBurgers.forEach( el => {
        el.addEventListener('click', () => {

          // Get the target from the "data-target" attribute
          const target = el.dataset.target;
          const $target = document.getElementById(target);

          // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
          el.classList.toggle('is-active');
          $target.classList.toggle('is-active');

        });
      });
    }

  });
}

export default {
  // mixins: [mobile],
  components: {
     Home,
     MobileHome,
     About,
     Ebook,
     Twitter,
     Youtube
  },
  data: {
  },
  methods: {
    getWidth () {
      return this.$vssWidth
    }
  },
  computed: {
  },
  mixins: [NuxtSSRScreenSize.NuxtSSRScreenSizeMixin],

   head: {
    script: [
      { src: 'vanta/three.min.js' },
      { src: 'vanta/p5.min.js' },
      { src: 'vanta/vanta.net.min.js' },
      { src: 'vanta/vanta.halo.min.js' },
      { src: 'vanta/vanta.trunk.min.js' },

]
  },
  async mounted() {
    if (process.browser) {
      window.THREE = THREE;
      const { default: NET } = await import("@/static/vanta/vanta.net.min.js");
      VANTA.NET({
        el: "#background",
        mouseControls: true,
        touchControls: true,
        gyroControls: false,
        // minHeight: 200.00,
        // minWidth: 200.00,
        scale: 1.00,
        scaleMobile: 1.00,
        color: 0x33a6eb,
        backgroundColor: 0xffffff,
        points: 8.00,
        maxDistance: 19.00,
        spacing: 16.00,
        showDots: false
      })
      VANTA.HALO({
        el: "#twitter",
        mouseControls: true,
        touchControls: true,
        gyroControls: false,
        // minHeight: 200.00,
        // minWidth: 200.00,
        xOffset: 0.04,
        size: 1.80
      })
      // VANTA.TRUNK({
      //   el: "#youtube",
      //   mouseControls: true,
      //   touchControls: true,
      //   gyroControls: false,
      //   // minHeight: 200.00,
      //   // minWidth: 200.00,
      //   scale: 1.00,
      //   scaleMobile: 1.00,
      //   spacing: 5.50,
      //   chaos: 7.00,
      //   color: 0xde99ad,
      //   backgroundColor: 0xd9d4cb,
      // })
    }
  },
}
</script>
<style lang="scss">
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  scroll-behavior: smooth;
}
.is-nav-text { 
  letter-spacing: 3px;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}


.sandwich-link a {
	padding: 12px 10px 10px;
	color: #566473;
	text-shadow: none;
	font-weight: 700;
}

.sandwich-link a::before,
.sandwich-link a::after {
	position: absolute;
	top: 100%;
	left: 0;
	width: 100%;
	height: 3px;
	background: #566473;
	content: '';
	-webkit-transition: -webkit-transform 0.3s;
	-moz-transition: -moz-transform 0.3s;
	transition: transform 0.3s;
	-webkit-transform: scale(0.85);
	-moz-transform: scale(0.85);
	transform: scale(0.85);
}

.sandwich-link a::after {
	opacity: 0;
	-webkit-transition: top 0.3s, opacity 0.3s, -webkit-transform 0.3s;
	-moz-transition: top 0.3s, opacity 0.3s, -moz-transform 0.3s;
	transition: top 0.3s, opacity 0.3s, transform 0.3s;
}

.sandwich-link a:hover::before,
.sandwich-link a:hover::after,
.sandwich-link a:focus::before,
.sandwich-link a:focus::after {
	-webkit-transform: scale(1);
	-moz-transform: scale(1);
	transform: scale(1);
}

.sandwich-link a:hover::after,
.sandwich-link a:focus::after {
	top: 0%;
	opacity: 1;
}
.has-shadow {
  padding: 8px 15px;
} 

.texti {
  transition: background-size .4s ease;
  background: linear-gradient(to bottom, transparent 62%, #d37766 0) center left/00% 30% no-repeat;
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;

  font-size: 1.33rem;
  font-weight: 000;
  letter-spacing: 3px;
  margin-left: 400px;
  width: 200px;
  height: 47px;
  color: #909ca8;
  cursor: pointer;   
    letter-spacing: .1rem;
    margin-right: 10px;
  &:hover {
    background-size: 100% 100%;
    color: rgba(70, 118, 250, 0.7);
  }
  &:active {
    background-size: 80% 100%;
  }
  &-container {
    z-index: 1;
    color: rgba(110, 151, 255, 0.7);
    position: relative;
    background-color: #fff;
    padding: 60px;
    box-shadow: 0 0 90px 10px rgba(255, 255, 255, 0.15);
  }
}
.icon_made {
      width: 1.8em; height: 1.8em;
      /* vertical-align: 6em; */
      fill: currentColor;
      // overflow: hidden;
      margin-top: 0em;
      margin-left: 0em;
    }
</style>
