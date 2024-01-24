<!-- HeaderComponent.vue -->

<template>
  <nav class="navbar navbar-light bg-light">
    <form class="container-fluid justify-content-start">
      <button class="btn btn-outline-success me-2" type="button">Main button</button>
      <button class="btn btn-sm btn-outline-secondary" type="button">
        Smaller button
      </button>
    </form>
  </nav>
</template>

<script>
export default {
  htmlCode: `<nav class="navbar navbar-light bg-light">
  <form class="container-fluid justify-content-start">
    <button class="btn btn-outline-success me-2" type="button">Main button</button>
    <button class="btn btn-sm btn-outline-secondary" type="button">Smaller button</button>
  </form>
</nav>`,
};
</script>

<style scoped>
/* Add any component-specific styles here */
</style>
