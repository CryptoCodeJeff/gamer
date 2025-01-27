<script lang="ts">
  import CA from '@/components/CA.svelte'
  import Socials from '@/components/Socials.svelte'
</script>

<style lang="scss">
  @use 'src/sass/mixins.scss' as *;

  .hero {
    border-top: 1px solid black;
    height: 100vh;
    background: linear-gradient(45deg, red, orange, yellow, green, blue, indigo, violet);
    background-size: 400% 400%;
    animation: rainbow 10s ease infinite;
    overflow: hidden;

    h1 {
      font-size: 200px;
      text-align: center;

      @include notDesktop {
        font-size: 60px;
      }
    }

    .te {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      margin: auto;
      width: 100%;
      max-width: 300px;
      filter: drop-shadow(0 0 20px rgb(255, 255, 255));

      animation: motionDog 1s 1s;
      transform-origin: bottom center;
    }

    @include notDesktop {
      .quickscope,
      .nyan,
      .doge,
      .gal,
      .chillguy {
        display: none;
      }
    }

    .quickscope {
      position: absolute;
      right: 10%;
      bottom: 0;
      width: 100%;
      max-width: 400px;
      z-index: 1;
    }

    .nyan {
      position: absolute;
      left: 0px;
      bottom: 20vh;
      width: 100%;
      max-width: 400px;
    }

    .doge {
      position: absolute;
      right: 0px;
      bottom: -100px;
      width: 100%;
      max-width: 400px;
    }

    .chillguy {
      position: absolute;
      top: -100px;
      max-width: 200px;
      transform: rotate(200deg);
    }

    .gal {
      position: absolute;
      bottom: -100px;
      left: 0;
      max-width: 200px;
      transform: rotate(20deg);
    }
  }

  @keyframes motionDog {
    0% {
      transform: rotateZ(-10deg);
    }
    20% {
      transform: rotateZ(10deg);
    }
    40% {
      transform: rotateZ(-10deg);
    }
    60% {
      transform: rotateZ(10deg);
    }
    80% {
      transform: rotateZ(-10deg);
    }
    100% {
      transform: rotateZ(0deg);
    }
  }

  @keyframes rainbow {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }
</style>

<div class="hero">
  <div class="g-wrapper">
    <h1>$GAMER</h1>
    <CA />

    <img class="te" src="/assets/gaming/te.png" alt="" />
    <img class="quickscope" src="/assets/gaming/quickscope.png" alt="" />
    <img class="nyan" src="/assets/gaming/nyan.gif" alt="" />
    <img class="doge" src="/assets/gaming/doge.png" alt="" />
    <img class="chillguy" src="/assets/gaming/chillguy.png" alt="" />
    <img class="gal" src="/assets/gaming/gal.png" alt="" />

    <Socials />
  </div>
</div>
