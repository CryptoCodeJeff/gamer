<script lang="ts">
  let ca = 'E6Afu2XpobyrE9m9FpctaZ6G4oXLLreUuZrVJ85cpump'
  let show = false

  const copy = () => {
    navigator.clipboard.writeText(ca)
    show = true

    setTimeout(() => (show = false), 1000)
  }
</script>

<style lang="scss">
  @use 'src/sass/mixins.scss' as *;

  button {
    position: relative;
    transition: 0.3s ease !important;
    text-align: center;
    width: 100%;
    font-size: 50px;

    @include notDesktop {
      font-size: 16px;
    }

    &:hover {
      box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.3);
      transform: scale(0.9);
    }
  }
</style>

<button class="link" on:click={copy}> {show ? 'Copied to clipboard!' : ca} </button>
