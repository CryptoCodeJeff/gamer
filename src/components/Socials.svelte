<script>
  import Svg from './Svg.svelte'
</script>

<style lang="scss">
  .socials {
    display: flex;
    gap: 50px;
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    width: fit-content;
    bottom: 20px;
    filter: drop-shadow(2px 2px 0 black);

    a {
      transition: 0.3s ease;
      &:hover {
        transform: scale(0.9);
      }
    }
  }
</style>

<div class="socials">
  <a href="https://t.me/tedgamer" target="_blank">
    <Svg name="telegram" width="50" height="50" fill="white" />
  </a>
  <a href="https://x.com/GAMER_CTO" target="_blank">
    <Svg name="twitter" width="50" height="50" fill="white" />
  </a>

  <a href="https://dexscreener.com/solana/9d1epmcxuv7e9grqpucviewavgguwhawqak5flkt1ana" target="_blank">
    <Svg name="dexscreener" width="50" height="50" fill="white" />
  </a>
</div>
