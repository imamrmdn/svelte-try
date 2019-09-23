<script>
  export let toggleSideBar;
</script>

<style>
  .backdrop {
    background: black;
    width: 100vw;
    height: 100vh;
    opacity: 0.5;
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    z-index: 1;
  }

  .drawer {
    background: #fff;
    position: absolute;
    top: 20;
    right: 10;
    left: 0;
    width: 15rem;
    height: 90vh;
    z-index: 1;
  }
</style>

<div>
  <div class="backdrop" on:click={toggleSideBar} />

  <div class="drawer" />
</div>
