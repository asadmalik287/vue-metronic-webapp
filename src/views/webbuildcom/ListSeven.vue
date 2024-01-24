<!-- HeaderComponent.vue -->

<template>
  <nav class="navbar navbar-light bg-light">
    <form class="container-fluid">
      <div class="input-group">
        <span class="input-group-text" id="basic-addon1">@</span>
        <input
          type="text"
          class="form-control"
          placeholder="Username"
          aria-label="Username"
          aria-describedby="basic-addon1"
        />
      </div>
    </form>
  </nav>
</template>

<script>
export default {
  htmlCode: `<nav class="navbar navbar-light bg-light">
  <form class="container-fluid">
    <div class="input-group">
      <span class="input-group-text" id="basic-addon1">@</span>
      <input type="text" class="form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
    </div>
  </form>
</nav>`,
};
</script>

<style scoped>
/* Add any component-specific styles here */
</style>
