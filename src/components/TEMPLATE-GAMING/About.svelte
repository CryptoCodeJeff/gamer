<script lang="ts">
</script>

<style lang="scss">
  @use 'src/sass/mixins.scss' as *;

  .section {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    background-color: rgb(0, 42, 104);
    min-height: 100vh;

    .g-wrapper {
      display: flex;
      gap: 100px;

      @include notDesktop {
        flex-direction: column-reverse;
      }

      .text {
        max-width: 600px;

        p,
        b {
          padding-bottom: 30px;
          font-family: 'Courier New', Courier, monospace;
        }

        a {
          background-color: #f3ec78;
          background-image: linear-gradient(45deg, #f3ec78, #af4261);
          background-size: 100%;
          -webkit-background-clip: text;
          -moz-background-clip: text;
          -webkit-text-fill-color: transparent;
          -moz-text-fill-color: transparent;
          text-shadow: none;
          font-size: 40px;
          font-weight: bold;
        }
      }

      video {
        border-radius: 20px;
        max-width: 350px;
        height: fit-content;
        box-shadow: 5px 5px 5px 0 rgba(0, 0, 0, 0.432);
        margin-bottom: 50px;

        @include notDesktop {
          max-width: 300px;
        }
      }
    }
  }
</style>

<div class="section">
  <h3 class="title" id="about">ABOUT</h3>

  <div class="g-wrapper">
    <video src="/assets/gaming/epico.mp4" autoplay controls loop></video>

    <div class="text">
      <p>
        An unofficial coin dedicated to <a href="https://x.com/TeTheGamer">TeTheGamer</a>
        was created, and the developer sent 70% of the total supply to TeTheGamer.
      </p>

      <p>
        As the memecoin began pumping, <a href="https://x.com/TeTheGamer">TeTheGamer</a> made the bold decision to burn 70% of the supply valued
        in millions rather than. This unprecedented move caused weak hands and panicked investors (jeeters) to nuke the price.
      </p>

      <p>
        Now, $GAMER aims to carry forward the powerful message <a href="https://x.com/TeTheGamer">TeTheGamer</a> left us:
      </p>

      <p>
        He is not our savior, <b>we are our own saviors</b>. A strong and united community can achieve the goals they set for themselves.
      </p>

      <p>In the world of crypto,<b>conviction and integrity are everything</b>.</p>

      <p>Let’s continue the legend of one of the greatest burns in crypto history and build something truly unforgettable. 🔥</p>
    </div>
  </div>
</div>
