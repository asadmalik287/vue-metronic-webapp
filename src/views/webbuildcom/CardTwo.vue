<!-- HeaderComponent.vue -->

<template>
  <div class="card bg-light shadow-sm">
    <div class="card-header">
      <h3 class="card-title">Title</h3>
      <div class="card-toolbar">
        <button type="button" class="btn btn-sm btn-light">Action</button>
      </div>
    </div>
    <div class="card-body card-scroll h-200px">Lorem Ipsum is simply dummy text...</div>
    <div class="card-footer">Footer</div>
  </div>
</template>

<script>
export default {
  htmlCode: ` <div class="card bg-light shadow-sm">
    <div class="card-header">
        <h3 class="card-title">Title</h3>
        <div class="card-toolbar">
            <button type="button" class="btn btn-sm btn-light">
                Action
            </button>
        </div>
    </div>
    <div class="card-body card-scroll h-200px">
        Lorem Ipsum is simply dummy text...
    </div>
    <div class="card-footer">
        Footer
    </div>
</div>`,
};
</script>

<style scoped>
/* Add any component-specific styles here */
</style>
