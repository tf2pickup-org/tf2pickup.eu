<script>
  /**
   * @type {string}
   */
  export let gamemode;

  /**
   * @type {?string}
   */
  export let href = null;
</script>

<div class="w-full h-full flex justify-center items-center gm{gamemode}">
  <div
    class="banner w-full h-1/2 min-h-[450px] flex flex-col flex-nowrap justify-center items-center relative"
  >
    <div class="block h-[40px] grow" />
    <div class="banner-text grow">
      <span class="banner-text__text relative z-0 text-[250px]">
        {gamemode}
        <span
          class="banner-text__shadow absolute left-0 bottom-[10px] z-[-1] text-[280px] tracking-wide"
          >{gamemode}</span
        >
      </span>
    </div>
    {#if href}
      <a
        {href}
        class="join-game-button block uppercase text-xl px-10 py-2 font-sans font-semibold hover:scale-[1.05] transition-transform duration-75"
      >
        Join the game!
        <span class="ml-2">→</span>
      </a>
    {:else}
      <span class="join-game-button block uppercase text-xl px-10 py-2 font-sans font-semibold">
        Coming soon
      </span>
    {/if}
  </div>
</div>

<style lang="scss">
  @mixin gamemode-banner($background-image-url, $text-color, $shadow-color) {
    background-image: url($background-image-url);
    background-size: cover;
    background-repeat: no-repeat;

    .banner {
      background-color: rgba(10, 26, 51, 0.7);

      .banner-text {
        .banner-text__text {
          color: $text-color;

          .banner-text__shadow {
            color: $shadow-color;

            -webkit-text-fill-color: transparent;
            -webkit-text-stroke-width: 1px;
            -webkit-text-stroke-color: $shadow-color;
          }
        }
      }

      .join-game-button {
        background: $text-color url('button_corner_yellow-01.svg') right bottom/14px no-repeat;
        color: #ffffff;
      }
    }
  }

  .gm9v9 {
    @include gamemode-banner('/9s_bg.png', #ea1557, #71afff);
  }

  .gm6v6 {
    @include gamemode-banner('/6s_bg.png', #71afff, #ea1557);
  }
</style>
