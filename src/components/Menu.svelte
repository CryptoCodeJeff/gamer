<script lang="ts">
  const items = [
    {
      title: 'History',
      link: '#historia',
    },
    {
      title: 'Buy',
      link: '#comprar',
    },
  ]
</script>

<style lang="scss">
  @use 'src/sass/global.scss' as *;

  .menu {
    position: sticky;
    display: flex;
    align-items: center;
    padding: 30px;
    margin: auto;
    gap: 60px;
    top: 10px;
    width: fit-content;
    margin-top: -200px;
    padding-bottom: 30px;

    @include notDesktop {
      gap: 30px;

      .item {
        width: 130px !important;
        h3 {
          font-size: 18px;
        }
      }

      img {
        margin-top: 15px;
      }
    }

    .item {
      position: relative;
      width: 150px;
      height: 100px;
      font-size: 24px;
    }

    h3 {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      background-image: url('/assets/paint.webp');
      background-color: white;
      text-align: center;
    }

    img {
      position: absolute;
      transform: rotate(90deg);
      top: -40px;
      width: 100%;
    }
  }
</style>

<div class="menu">
  {#each items as item}
    <a class="item" href={item.link}>
      <img src="/assets/marco.png" alt="" />

      <h3>
        {item.title}
      </h3>
    </a>
  {/each}
</div>
