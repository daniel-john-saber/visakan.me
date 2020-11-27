<template>
  <div class="is-transparent hero-body" >
      <div class="container has-text-centered">
        <h2 class="is-subtitle">
        {{ this.$vssHeight }}
          presenting my best work . . .  
        </h2>
        <div class="columns">
          <div class="column is-two-fifths">
            <div class="hero is-fullheight">
              <img class="vv-cover" src="~/assets/vv_media_cover.png" width="800" height="auto" itemprop="image">
            </div>
          </div>
          <div class="column is-one-half" style="border-top: 2px solid black;">
            <div v-if="getWidth() > 900">
              <div class="container" style="vertical-align: middle; display: inline-block;">
                <div style="margin-top: 1.3em;">
                  <a class="text-secret"  src="https://gumroad.com/l/friendlynerdbook"><em>friendly<br>ambitious<br>nerd </em> </a>
                </div>
              </div>
              <div class="line-two"></div>
            </div>
            <div v-else style="margin-top: -15em; margin-bottom: 25em;">
              <img src="~/assets/vv_mobile_title.png" width="auto" height="auto" itemprop="image">
            </div>
          </div>
          <!-- <div class="column is-one-half is-centered has-nice-link">
          </div> -->
        </div>
        <div v-if="this.$vssHeight > 900" class="columns" style="margin-top: -35em;">
              <card
                title="a whopping 39 essays"
                image="essays.png"
              >
                Riffs about creativity, taste, culture and so much more
              </card>
              <card
                title="totaling over 100 pages"
                image="pages.png"
              >
                Powerful, hard hitting content — without the filler 
              </card>
              <card
                title="and 40 awesome chapters"
                image="chapters.png"
              >
                Everything from Ambition to Friendship to Marriage 
              </card>
          </div>
          <div v-else class="columns" style="margin-top: -25em;">
              <card
                title="a whopping 39 essays"
                image="essays.png"
              >
                Riffs about creativity, taste, culture and so much more
              </card>
              <card
                title="totaling over 100 pages"
                image="pages.png"
              >
                Powerful, hard hitting content — without the filler 
              </card>
              <card
                title="and 40 awesome chapters"
                image="chapters.png"
              >
                Everything from Ambition to Friendship to Marriage 
              </card>
          </div>
          <div class="columns is-vcentered is-centered" style="margin-top: 5em;">
            <div class="column is-narrow is-centered">
              <a href="https://gumroad.com/l/friendlynerdbook" target="blank">
                <button class="button">
                  <svg class="iconi" aria-hidden="true" style="margin-top: -2.5em;">
                    <use xlink:href="#icon-gumroad"></use>
                  </svg>
                  <!-- <div> -->
                    Buy Now!
                  <!-- </div> -->
                  <div class="button__horizontal"></div>
                  <div class="button__vertical"></div>
                </button>
              </a>
            </div>
          </div>
      </div>
  </div>
</template>
<script>
import Card from '~/components/Card'
import NuxtSSRScreenSize from 'nuxt-ssr-screen-size'

export default {
   components: {
    Card,

   },
  mixins: [NuxtSSRScreenSize.NuxtSSRScreenSizeMixin],  
  methods: {
    getWidth () {
      return this.$vssWidth
    }
  },
  // async mounted() {
  //   // window is only avaiable on browser
  //   if (process.browser) {
  //     window.THREE = THREE;
  //     const { default: CLOUDS } = await import("@/static/vanta/vanta.clouds.min.js");
  //     VANTA.CLOUDS({
  //       el: "#section-background",
  //       mouseControls: true,
  //       touchControls: true,
  //       gyroControls: false,
  //       minHeight: 2200.00,
  //       minWidth: 800.00,
  //       cloudColor: 0xa4a4c0,
  //       sunColor: 0x98653f,
  //       speed: 0.10
  //     })
  //   }
  // },
};
</script>
<style scoped lang='scss'>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@1,500&display=swap');

.text-secret {
  margin-top: 5em;
  transition: background-size .4s ease;
  // background: linear-gradient(to bottom, transparent 62%, #d37766 0) center left/00% 30% no-repeat;
  font-family: 'Helvetca Neue', sans-serif; 
  font-size: 6.5em; 
  font-weight: bold; 
  letter-spacing: -1px; 
  line-height: 1; 
  text-align: center; 
  width: 200px;
  color: #28292b;
  cursor: pointer;
    letter-spacing: .1rem;
    margin-right: 10px;
  &:hover {
    background-size: 100% 100%;
    color: rgba(70, 118, 250, 0.7);
    // background: #ffb7b7; 
  }
 
  // &-container {
  //   z-index: 1;
  //   color: rgba(110, 151, 255, 0.7);
  //   position: absolute;
  //   background-color: #fff;
  //   padding: 0px;
  //   box-shadow: 0 0 90px 10px rgba(255, 255, 255, 0.15);
  // }
}

.is-subtitle { 
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  font-family: 'Montserrat', sans-serif;  /* padding-bottom: 5px; */
  margin-bottom: 1em;
}
.vv-cover { 
  /* margin: 0px;
  padding: 0px; */
  max-height: 100%;
  left:0;
  right:0;
  margin:0 auto;
}

.line-one {
  margin-top: 1em;
  /* margin: 0 auto; */
  width: 50%;
  height: 0px;
  border-bottom: 2px solid black;
  position: absolute;
  padding-left: 70px 0;
}
.line-two {
  margin-top: 3em;
  /* margin: 0 auto; */
  width: 100%;
  height: 0px;
  border-bottom: 2px solid black;
  // position: absolute;
  padding-left: 70px 0;
}

.iconi {
      width: 1.2em; height: 1.2em;
      /* vertical-align: 6em; */
      fill: currentColor;
      // overflow: hidden;
      margin-top: 0em;
      margin-left: 0em;
    }

//fancy button
.button {
	
	--offset: 10px;
	--border-size: 2px;
	
	display: block;
	position: relative;
	padding: 1.5em 1em;
	appearance: none;
	border: 0;
	background: transparent;
	color: #e55743;
	text-transform: uppercase;
	letter-spacing: .25em;
	outline: none;
	cursor: pointer;
	font-weight: bold;
	border-radius: 0;
	box-shadow: inset 0 0 0 var(--border-size) currentcolor;
	transition: background .8s ease;
	
	&:hover {
		background: rgba(100, 0, 0, .03);
	}
	
	&__horizontal,
	&__vertical {
		position: absolute;
		top: var(--horizontal-offset, 0);
		right: var(--vertical-offset, 0);
		bottom: var(--horizontal-offset, 0);
		left: var(--vertical-offset, 0);
		transition: transform .8s ease;
		will-change: transform;
		
		&::before {
			content: '';
			position: absolute;
			border: inherit;
		}
	}
	
	&__horizontal {
		--vertical-offset: calc(var(--offset) * -1);
		border-top: var(--border-size) solid currentcolor;
		border-bottom: var(--border-size) solid currentcolor;
		
		&::before {
			top: calc(var(--vertical-offset) - var(--border-size));
			bottom: calc(var(--vertical-offset) - var(--border-size));
			left: calc(var(--vertical-offset) * -1);
			right: calc(var(--vertical-offset) * -1);
		}
	}
	
	&:hover &__horizontal {
		transform: scaleX(0);
	}
	
	&__vertical {
		--horizontal-offset: calc(var(--offset) * -1);
		border-left: var(--border-size) solid currentcolor;
		border-right: var(--border-size) solid currentcolor;
		
		&::before {
			top: calc(var(--horizontal-offset) * -1);
			bottom: calc(var(--horizontal-offset) * -1);
			left: calc(var(--horizontal-offset) - var(--border-size));
			right: calc(var(--horizontal-offset) - var(--border-size));
		}
	}
	
	&:hover &__vertical {
		transform: scaleY(0);
	}
	
}
</style>
