<script>
  let isOpen = false;

  const toggle = () => {
    isOpen = !isOpen;
  };

  $: console.log(isOpen);
</script>

<div class="menu-bar">
  <div class="menu-wrapper" class:open={isOpen}>
    <div on:click={toggle} class="btn-menu">☰</div>
    <div class="menu-container">
      <slot />
    </div>
  </div>
</div>

<style>
  .menu-bar {
    outline: solid 1px orange;
  }

  .menu-wrapper {
    position: relative;
    display: flex;
    flex-direction: row;
    padding: 4px;
  }

  .btn-menu {
    display: none;
    flex: 0 0 auto;
    cursor: pointer;
  }
  .menu-container {
    flex: 0 1 auto;
  }

  @media (max-width: 600px) {
    .btn-menu {
      display: inline;
      outline: solid 1px blue;
    }

    .menu-wrapper {
      position: relative;
      flex-direction: column;
    }

    .menu-wrapper.open {
      position: fixed;
      top: 0;
      bottom: 0;
      left: 0;
      right: 25%;
    }

    .menu-container {
      display: none;
    }

    .menu-wrapper.open .menu-container {
      position: fixed;
      top: 0;
      bottom: 0;
      left: 0;
      right: 25%;
      background-color: #9cf;
      /* min-width: 50%;
      max-width: 75%; */
    }

    .menu-container :global(ul) {
      flex-direction: column;
    }
  }
</style>
