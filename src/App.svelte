<script>
  import Menu from "./components/Menu.svelte";
</script>

<svelte:head><title>Menu</title></svelte:head>

<header>
  <nav>
    <Menu>
      <ul>
        <li><a href="/">Item 1</a></li>
        <li><a href="/">Item 2</a></li>
        <li><a href="/">Item 3</a></li>
        <li><a href="/">Item 4</a></li>
      </ul>
    </Menu>
  </nav>
</header>

<main>
  <p>Lorem ipsum.</p>
</main>

<style>
  ul {
    list-style-type: none;
    padding: 0;
  }
  a {
    text-decoration: none;
    color: inherit;
  }

  header {
    border-bottom: 1px solid #e2e8f0;
  }

  nav {
    display: flex;
    padding: 1rem 0;
  }
</style>
