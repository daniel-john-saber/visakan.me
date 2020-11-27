<template>
  <div class="columns is-1 is-centered" style="margin-top:4em;">
    <div class="column is-one-fifth">
      <!-- <div class="vv-container"> -->
        <a href="https://gumroad.com/l/friendlynerdbook" target="_blank" class="vv-btn">
          <svg class="iconi" aria-hidden="true">
            <use xlink:href="#icon-Notebook"></use>
          </svg>
          <svg>
            <defs>
                <linearGradient id="grad1">
                    <stop offset="0%" stop-color="#FF8282"/>
                    <stop offset="100%" stop-color="#E178ED" />
                </linearGradient>
            </defs>
            <rect x="5" y="5" rx="25" fill="none" stroke="url(#grad1)" width="200" height="50"></rect>
          </svg>
          <span style="margin-left:-2em;">Ebook</span>
        </a>
      </div>
      <div class="column is-one-fifth">
        <a href="https://twitter.com/visakanv" target="_blank" class="vv-btn">
            <svg class="iconi" aria-hidden="true">
                <use xlink:href="#icon-twitter"></use>
            </svg>
            <svg>
              <defs>
                  <linearGradient id="grad1">
                      <stop offset="0%" stop-color="#FF8282"/>
                      <stop offset="100%" stop-color="#E178ED" />
                  </linearGradient>
              </defs>
              <rect x="5" y="5" rx="25" fill="none" stroke="url(#grad1)" width="200" height="50"></rect>
            </svg>
            
            <span style="margin-left:-2em;">Twitter</span>
          </a>
        </div>
        <div class="column is-one-fifth">
        <a href="youtube.com/visakanv" target="_blank" class="vv-btn">
            <svg class="iconi" aria-hidden="true">
                <use xlink:href="#icon-youtube1"></use>
            </svg>
            <svg>
              <defs>
                  <linearGradient id="grad1">
                      <stop offset="0%" stop-color="#FF8282"/>
                      <stop offset="100%" stop-color="#E178ED" />
                  </linearGradient>
              </defs>
              <rect x="5" y="5" rx="25" fill="none" stroke="url(#grad1)" width="200" height="50"></rect>
            </svg>
            
            <span style="margin-left:-2em;">Youtube</span>
          </a>
        </div>
  </div>
</template>

<script>
</script>

<style scoped>
  .iconi {
    width: 2em; height: 2em;
    /* vertical-align: 6em; */
    fill: currentColor;
    overflow: hidden;
    margin-top: 0.7em;
    margin-left: 2em;
  }
  .vv-butt-container{
    height:100%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding-right: 5em;
  }
  .vv-btn {
    margin-top: 2em;
    position: relative;
    display: inline-block;
    width: 277px;
    height: 50px;
    font-size: 1em;
    font-weight: bold;
    line-height: 60px;
    text-align: center;
    text-transform: uppercase;
    background-color: transparent;
    cursor: pointer;
    text-decoration:none;
    font-family: 'Roboto', sans-serif;
    font-weight:900;
    font-size:17px;
    letter-spacing: 0.045em;
    margin-right: 1em;
  }

  .vv-btn svg {
      position: absolute;
      top: 0;
      left: 0;
  }

  .vv-btn svg rect {
      stroke-width: 4;
      stroke-dasharray: 353, 0;
      stroke-dashoffset: 0;
      -webkit-transition: all 600ms ease;
      transition: all 600ms ease;
  }

  .vv-btn span{
    background: rgb(255,130,130);
    background: -moz-linear-gradient(left,  rgba(255,130,130,1) 0%, rgba(225,120,237,1) 100%);
    background: -webkit-linear-gradient(left,  rgba(255,130,130,1) 0%,rgba(225,120,237,1) 100%);
    background: linear-gradient(to right,  rgba(255,130,130,1) 0%,rgba(225,120,237,1) 100%);
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ff8282', endColorstr='#e178ed',GradientType=1 );
    
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .vv-btn:hover svg rect {
      stroke-width: 4;
      stroke-dasharray: 196, 543;
      stroke-dashoffset: 437;
  }
</style>

