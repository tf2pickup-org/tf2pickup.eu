<script>
  import GamemodeBanner from '@components/gamemode-banner.svelte';
  import logo from '@static/tf2pickup.eu_logo_text-01.png';
</script>

<header class="header p-3">
  <img src={logo} alt="tf2pickup.eu logo" class="h-[40px]" />
</header>

<main class="grow w-100">
  <div class="h-full columns-2 gap-0">
    <GamemodeBanner gamemode="9v9" href="https://hl.tf2pickup.eu/" />
    <GamemodeBanner gamemode="6v6" />
  </div>
</main>

<style lang="scss">
  header {
    background-color: #0a1a33;
  }
</style>
