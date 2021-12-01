<script>
  let isOpen = false;

  const toggle = () => {
    isOpen = !isOpen;
  };

  $: console.log(isOpen);
</script>

<!-- Based on: https://dev.to/devggaurav/let-s-build-a-responsive-navbar-and-hamburger-menu-using-html-css-and-javascript-4gci -->

<div on:click={toggle} class="btn" role="button">☰</div>
<slot />

<style>
  .btn {
    display: none;
    cursor: pointer;
  }

  :global(ul) {
    display: flex;
    flex-direction: row;
    outline: solid 1px blue;
  }

  :global(ul > li) {
    margin-right: 4px;
    outline: solid 1px red;
  }
</style>
