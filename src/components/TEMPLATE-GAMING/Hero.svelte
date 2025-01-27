<script lang="ts">
  import CA from '@/components/CA.svelte'
  import Socials from '@/components/Socials.svelte'
</script>

<style lang="scss">
  @use 'src/sass/mixins.scss' as *;

  .hero {
    border-top: 1px solid black;
    height: 100vh;
    background-image: url('/assets/gaming/gamingte.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: bottom;
    overflow: hidden;

    h1 {
      font-size: 200px;
      text-align: center;

      @include notDesktop {
        font-size: 60px;
      }
    }

    .bg {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      object-fit: cover;
      object-position: bottom;
    }

    .nyan {
      position: fixed;
      bottom: 30vh;
      left: 0;

      @include notDesktop {
        display: none;
      }
    }
    .snop {
      position: fixed;
      bottom: 0px;
      right: 10px;
      width: 150px;

      @include notDesktop {
        display: none;
      }
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
</style>

<div class="hero">
  <h1>$GAMER</h1>
  <CA />
  <img class="nyan" src="/assets/gaming/nyan.gif" alt="" />
  <img class="snop" src="/assets/gaming/snop.gif" alt="" />

  <Socials />
</div>
