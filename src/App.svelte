<script>
  import Menu from "./components/Menu.svelte";
</script>

<svelte:head><title>Menu</title></svelte:head>

<main>
  <Menu>
    <ul>
      <li><a href="/">Item 1</a></li>
      <li><a href="/">Item 2</a></li>
      <li><a href="/">Item 3</a></li>
      <li><a href="/">Item 4</a></li>
    </ul>
  </Menu>

  <p>Lorem ipsum.</p>
</main>

<style>
  ul {
    list-style-type: none;
    padding: 0;
    display: flex;
    flex-direction: row;
  }

  li {
    flex: 0 0 auto;
    outline: solid 1px red;
  }
  a {
    display: block;
    padding: 2px 4px;
    text-decoration: none;
    color: inherit;
  }
</style>
