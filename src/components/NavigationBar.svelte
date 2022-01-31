<script>
  import NavigationBarListItems from './NavigationBarItems/NavigationBarListItems.svelte';
  let src = 'resources/hh-logo.svg';
</script>

<nav>
  <div class="brand-logo">
    <a href="/"><img {src} alt="Home Hardware" width="40" height="40" /></a>
  </div>
  <div class="search-box">
    <input type="search" placeholder="Search" />
    <button><i class="fas fa-search" /></button>
  </div>
  <NavigationBarListItems />
</nav>

<style>
  nav {
    background-color: #e4002b;
    height: 70px;
    display: flex;
    align-items: center;
  }
  .brand-logo {
    margin-left: 90px;
  }
  .brand-logo a {
    display: inline-block;
  }
  .search-box {
    position: relative;
    display: inline-block;
    padding-top: 5px;
    margin: 0 50px;
  }
  input[type='search'] {
    border-radius: 20px;
    width: 400px;
    padding-left: 20px;
  }
  .search-box button {
    border: none;
    padding: 0;
  }
  .search-box button i {
    color: red;
    position: absolute;
    right: 16px;
    top: 16px;
  }
</style>
