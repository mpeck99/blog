<template>
  <header class="main-header">
    <nav class="main-nav">
      <ul class="nav-links">
        <nuxt-link to="/" tag="li" class="nav-link"><a>Home</a></nuxt-link>
        <nuxt-link to="/about" tag="li" class="nav-link"><a>About</a></nuxt-link>
        <nuxt-link to="/recipes" tag="li" class="nav-link"><a>Recipes</a></nuxt-link>
        <nuxt-link to="/family" tag="li" class="nav-link"><a>Family</a></nuxt-link>
        <nuxt-link to="/pets" tag="li" class="nav-link"><a>Pets</a></nuxt-link>
        <nuxt-link to="/health" tag="li" class="nav-link"><a>Health</a></nuxt-link>
      </ul>
    </nav>
  </header>
</template>

<style scoped>

    .main-header{
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 4.5rem;
    }
    .main-nav{
      height: 100%;
    }
    .nav-links{
      list-style: none;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100%;
    }
    .nav-link{
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 0 1rem;
      padding: 0.3rem;

    }
    .nav-link.nuxt-link-exact-active {
      border-bottom: 2px solid rebeccapurple;

    }
    .nav-link a{
      display: block;
      text-decoration: none;
    }
    .nav-link a:hover,
    .nav-link a:active,
    .nav-link.nuxt-link-exact-active a{
    color: rebeccapurple;
    }
</style>

