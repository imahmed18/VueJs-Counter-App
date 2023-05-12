<script setup>
import HelloWorld from "../components/HelloWorld.vue";
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
      <HelloWorld msg="Vue Counter App" />
    </div>
  </header>
</template>

<style scoped>
header {
  margin: auto;
  width: 50%;
  padding: 10px;

  justify-content: center;
  align-items: center;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.nav-links {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

.nav-links a.router-link-exact-active {
  color: var(--color-text);
}

.nav-links a.router-link-exact-active:hover {
  background-color: transparent;
}

.nav-links a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

.nav-links a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }

  .nav-links {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
