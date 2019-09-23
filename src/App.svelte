<script>
  import SideBar from "./SideBar.svelte";

  let showSideBar = false;

  function toggleSideBar() {
    showSideBar = !showSideBar;
  }
</script>

<style>
  nav {
    background: #eb3d34;
  }
  .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 0 2rem;
    height: 10vh;
  }
  .row {
    display: flex;
    flex-direction: row;
  }

  div p {
    padding: 0 0.5rem;
    color: #fff;
    font-size: 1.1rem;
    font-weight: 500;
    cursor: pointer;
  }
</style>

<div>
  <nav>
    <div class="container">

      <p on:click={toggleSideBar}>
        <i class="fi-cnlrxl-barcode-solid" />
      </p>

      <div class="row">
        <p class="item">Sign in</p>
        <p class="item">Sign up</p>
      </div>
    </div>
  </nav>
  {#if showSideBar}
    <SideBar {toggleSideBar} />
  {/if}

</div>
