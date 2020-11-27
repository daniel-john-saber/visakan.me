<template>
  <div  class="container text-is-centered" style="margin-left: 13em; height: 10em;">
    <h1 class="vv-title"><span>Visakan Veersamy</span></h1>
    <div class="blobs_1"></div>
    <div class="blobs_2"></div>
    <div class="blobs_3"></div>
    <div class="blobs_4"></div>
    <div class="blobs_5"></div>
    <div class="blobs_6"></div>
    <div class="blobs_7"></div>
    <div class="blobs_8"></div>
    <div class="blobs_9"></div>
    <div class="blobs_10"></div>
    <div class="blobs_11"></div>
  </div>
</template>
<script>
export default { 
  
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Montserrat:900i&display=swap');
@import url('https://fonts.googleapis.com/css?family=Titan+One');

  body{text-align:center}
  div{display:block;position:absolute}

  /* .vv-title-container { */
    /* width:320px;
    height:320px; */
    /* top:50%;
    left:50%;
    transform:translate(-50%,-50%)
    } */

  .vv-title{
    background:#fff;
    width:100%;
    height:100%;
    margin:0;
    padding:0;
    display:flex;
    font-family:'Titan One',cursive;
    font-size:90px;
    font-weight:700;
    flex-flow:row wrap;
    align-content:center;
    justify-content:center
    }

  .vv-title span{width:100%;position:relative}

  .vv-title span:before{
    background:linear-gradient(45deg,#fc5c7d,#6a82fb,#fc5c7d);
    width:100%;
    height:100%;
    display:block;
    position:absolute;
    content:"";
    mix-blend-mode:screen
    }

  [class*="blobs"]
    {mix-blend-mode:color;animation:blobs 15s ease-in-out infinite alternate}

  .blobs_1{
    background:#ff1493;
    width:60px;
    height:60px;
    top:90px;
    left:210px
    }

  .blobs_2{
    background:#ffdd95;
    width:80px;
    height:80px;
    top:64px;
    left:430px
    }

  .blobs_3{
    background:#00ff00;
    width:60px;
    height:60px;
    top:90px;
    left:20px
    }

  .blobs_4{
    background:#ff0000;
    width:100px;
    height:50px;
    top:40px;
    left:480px
    }

  .blobs_5{
    background:#ffff00;
    width:50px;
    height:50px;
    top:55px;
    left:70px
    }
    

  .blobs_6{
    background:#00ffff;
    width:60px;
    height:50px;
    top:85px;
    left:85px
    }

  .blobs_7{
    background:#ff8c00;
    width:50px;
    height:50px;
    top:30px;
    left:180px
    }
  .blobs_8{
    background:#00a2ff;
    width:60px;
    height:50px;
    top:75px;
    left:585px
    }
  .blobs_9{
    background:#ff20f4;
    width:50px;
    height:50px;
    top:30px;
    left:680px
    }
  .blobs_10{
    background:#ffff00;
    width:50px;
    height:50px;
    top:55px;
    left:710px
    }
    

  .blobs_11{
    background:#01ffff;
    width:60px;
    height:50px;
    top:85px;
    left:785px
    }

  @keyframes blobs{
    0%{border-radius:26% 74% 61% 39% / 54% 67% 33% 46%}
    10%{border-radius:74% 26% 47% 53% / 68% 46% 54% 32%}
    20%{border-radius:48% 52% 30% 70% / 27% 37% 63% 73%}
    30%{border-radius:73% 27% 57% 43% / 28% 67% 33% 72%}
    40%{border-radius:63% 37% 56% 44% / 25% 28% 72% 75%}
    50%{border-radius:39% 61% 70% 30% / 61% 29% 71% 39%}
    60%{border-radius:27% 73% 29% 71% / 73% 51% 49% 27%}
    70%{border-radius:39% 61% 65% 35% / 74% 65% 35% 26%}
    80%{border-radius:55% 45% 37% 63% / 38% 30% 70% 62%}
    90%{border-radius:25% 75% 70% 30% / 39% 50% 50% 61%}
    100%{border-radius:66% 34% 33% 67% / 65% 73% 27% 35%}
    }

</style>