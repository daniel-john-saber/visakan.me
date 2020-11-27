<template>
  <section>
    <div class="hero-body" style="margin-top: 8em;" >
      <div class="container has-text-centered">
        <div class="columns is-vcentered">
          <div class="column is-centered is-one-half is-centered" style="padding-bottom: 4em;">
            <p class="block vv-subtitle " style="margin-bottom: 0em;"> 
              Hi, I'm Visa - The Internet's
            </p>
            <div v-if="getWidth() > 1410">
              <span class="vv-title underline--magical">
                FRIENDLY AMBITIOUS NERD!
              </span>
            </div>
            <div v-else>
              <img src="~/assets/vv_friendly.png" width="auto" height="auto" itemprop="image">

            </div>
            <div class="columns is-2 is-centered" style="margin-top: 2em; margin-bottom: -2em;">
              <div class="column is-3" style="margin-left:2em;">
                <div class="glass-container">
                  <svg class="iconi" aria-hidden="true">
                    <use xlink:href="#icon-xiaoxiong"></use>
                  </svg>
                  <p class="vv-pp">cheeky & playful vibes!</p>
                </div>
              </div>
              <div class="column is-3 is-centered" style="margin-left:2em;">
                <div class="glass-container">
                  <svg class="iconi" aria-hidden="true">
                    <use xlink:href="#icon-reqiqiu"></use>
                  </svg>
                  <p class="vv-pp">joyfully unlearning coercion</p>
                </div>
              </div>
              <div class="column is-3 is-centered" style="margin-left:2em;">
                <div class="glass-container">
                  <svg class="iconi" aria-hidden="true">
                    <use xlink:href="#icon-denglong"></use>
                  </svg>
                  <p class="vv-pp">publicly, in real-time</p>
                </div>
              </div>
            </div>
            <h1 style="margin-top: 8em; margin-bottom: -4em;" class="vv-pp">Check out my ebook!</h1>
            <a href="#ebook" class="arrow" style="margin-bottom: 10em;">
                <span></span>
                <span></span>
                <!-- <span></span> -->
            </a> 
          </div>
        </div>
      </div>
  </div>
  </section>
</template>
<script>
import NuxtSSRScreenSize from 'nuxt-ssr-screen-size'

export default {
  mixins: [NuxtSSRScreenSize.NuxtSSRScreenSizeMixin],
  methods: {
    getWidth () {
      return this.$vssWidth
    }
  },
}
</script>
<style scoped lang="less">
@import url('https://fonts.googleapis.com/css?family=Titan+One');
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');
.underline--magical {
  width: 10em;
  background-image: linear-gradient(120deg, #ffc3ac 0%, #6386f8 90%);
  background-repeat: no-repeat;
  background-size: 85% 0.3em;
  background-position: 49% 88%;
  transition: background-size 0.25s ease-in;
  &:hover {
    background-size: 94% 88%;
  }
}
.glass-container {
    width: 20rem;
    height: auto;
    box-shadow: 0 0 1rem 0 rgba(0, 0, 0, .2);
    border-radius: 15px;
    position: relative;
    z-index: 1;
    background: inherit;
    overflow: hidden;
  }

  .glass-container:before {
    content: "";
    position: absolute;
    background: inherit;
    z-index: -1;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    box-shadow: inset 0 0 2000px rgba(255, 255, 255, .5);
    filter: blur(10px);
    margin: -20px;
  }
  
  .vv-pp { 
     font-family: 'Montserrat', sans-serif; 
     margin-bottom: 1em;

  }
  .vv-subtitle{

    // background:#fff;
    width:100%;
    height:100%;
    margin:0;
    padding:0;
    display:flex;
    font-family:'Titan One',cursive;
    font-size:45px;
    font-weight:300;
    flex-flow:row wrap;
    align-content:center;
    justify-content:center;
    color: #534145
  }
  .vv-title{
    // background:#fff;
    width:auto;
    height:100%;
    margin:0;
    padding:0;
    display:flex;
    font-family:'Titan One',cursive;
    font-size:80px;
    font-weight:600;
    flex-flow:row wrap;
    align-content:center;
    justify-content:center;
    color: #d15d74

  }
  .vv-title span:before{
    background:linear-gradient(45deg,#fc5c7d,#6a82fb,#fc5c7d);
    width:100%;
    height:100%;
    display:block;
    position:absolute;
    content:"";
    mix-blend-mode:screen
    }
  .vv-title span{width:100%;position:relative}
  .iconi {
      width: 4em; height: 4em;
      /* vertical-align: 6em; */
      fill: currentColor;
      overflow: hidden;
      margin-top: 0.7em;
      margin-left: 2em;
    }
    // body {
    //   font-family: 'Poppins', sans-serif;
    //   margin: 0;
    //   padding: 0;
    //   display: flex;
    //   flex-direction: column;
    //   justify-content: center;
    //   align-items: center;
    //   min-height: 100vh;
    //   -webkit-font-smoothing: antialiased;
    //   -moz-osx-font-smoothing: grayscale;
    // }


.glass-container:hover {
  opacity: 1;
  background: #e2a9e5;
  background: -moz-linear-gradient(-45deg, #e2a9e5 15%, #2b94e5 100%);
  background: -webkit-linear-gradient(-45deg, #e2a9e5 15%,#2b94e5 100%);
  background: linear-gradient(135deg, #e2a9e5 15%,#2b94e5 100%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#e2a9e5', endColorstr='#2b94e5',GradientType=1 );
}

.about-boxes .box.box2:hover,
.about-boxes .box.box2:hover~.bg {
  opacity: 1;
  background: #632c65;
  background: -moz-linear-gradient(-45deg, #632c65 15%, #56a5e2 100%);
  background: -webkit-linear-gradient(-45deg, #632c65 15%,#56a5e2 100%);
  background: linear-gradient(135deg, #632c65 15%,#56a5e2 100%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#632c65', endColorstr='#56a5e2',GradientType=1 );
}

.about-boxes .box.box3:hover,
.about-boxes .box.box3:hover~.bg {
  opacity: 1;
  background: #4b384c;
  background: -moz-linear-gradient(-45deg, #4b384c 15%, #da5de2 100%);
  background: -webkit-linear-gradient(-45deg, #4b384c 15%,#da5de2 100%);
  background: linear-gradient(135deg, #4b384c 15%,#da5de2 100%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#4b384c', endColorstr='#da5de2',GradientType=1 );
}

.things > .content {
  float: left;
  width: 50%;
  height: 500px;
  -webkit-box-sizing: border-box; 
	-moz-box-sizing: border-box;    
	box-sizing: border-box;
  position: relative;
}

.things > .content h1 {
  font-family: 'Montserrat', sans-serif; 
  text-transform: uppercase;
  top: 0;
  bottom: 0;
  left: -200;
  right: 200;
  margin: auto;
  position: absolute;
  height: 150px;
  margin-left: -10em;
  color: rgb(48, 41, 41);
}

/* Arrow */
.arrow{
    position: absolute;
    top: 100%;
    margin-top: 3em;
    left: 50%;
    transform: translate(-50%,-50%);
}
.arrow span{
    display: block;
    width: 30px;
    height: 30px;
    border-bottom: 5px solid #06A8FF;
    border-right: 5px solid #06A8FF;
    transform: rotate(45deg);
    margin: -10px;
    animation: animate 2s infinite;
}
.arrow span:nth-child(2){
    animation-delay: -0.2s;
}
.arrow span:nth-child(3){
    animation-delay: -0.4s;
}
@keyframes animate {
    0%{
        opacity: 0;
        transform: rotate(45deg) translate(-20px,-20px);
    }
    50%{
        opacity: 1;
    }
    100%{
        opacity: 0;
        transform: rotate(45deg) translate(20px,20px);
    }
}
</style>