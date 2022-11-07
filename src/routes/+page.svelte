<header class="header p-3">
  <img src="tf2pickup.eu_logo_text-01.png" alt="tf2pickup.eu logo" class="h-[40px]" />
</header>

<main class="gap-0.5 columns-2 w-full h-full">
  <div class="w-full h-full flex justify-center items-center gm9v9">
    <div class="banner w-full h-1/2 min-h-[450px] flex flex-col flex-nowrap justify-center items-center pt-9 relative">
      <div class="banner-text grow">
        <span class="banner-text__text relative z-0 text-[250px]">
          9v9
          <span class="banner-text__shadow absolute left-0 bottom-[10px] z-[-1] text-[280px] tracking-wide">9v9</span>
        </span>
      </div>
      <a href="https://9v9.tf2pickup.eu" class="join-game-button block uppercase text-xl hover:scale-[1.05] transition-transform duration-75 font-sans font-semibold">
        Join the game!
        <span class="ml-2">→</span>
      </a>
    </div>
  </div>
  <div class="w-full h-full flex justify-center items-center gm6v6">
    <div class="banner w-full h-1/2 min-h-[450px] flex flex-col flex-nowrap justify-center items-center pt-9 relative">
      <div class="banner-text grow">
        <span class="banner-text__text relative z-0 text-[250px]">
          6v6
          <span class="banner-text__shadow absolute left-0 bottom-[10px] z-[-1] text-[280px] tracking-wide">6v6</span>
        </span>
      </div>
      <span class="join-game-button block uppercase font-sans font-semibold">
        Coming soon
      </span>
    </div>
  </div>
</main>

<style lang="scss">
  @mixin gamemode-banner($background-image-url, $text-color, $shadow-color) {
    background-image: url($background-image-url);

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
        padding: 5px 40px;
      }
    }
  }

  header {
    background-color: #0a1a33;
    color: #ffffff;
  }

  .gm9v9 {
    @include gamemode-banner('9s_bg.png', #ea1557, #71afff);
  }

  .gm6v6 {
    @include gamemode-banner('6s_bg.png', #71afff, #ea1557);
  }
</style>
