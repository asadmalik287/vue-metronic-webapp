<!-- HeaderComponent.vue -->

<template>
  <div class="card shadow-sm">
    <div
      class="card-header collapsible cursor-pointer rotate"
      data-bs-toggle="collapse"
      data-bs-target="#kt_docs_card_collapsible"
    >
      <h3 class="card-title">Title</h3>
      <div class="card-toolbar rotate-180">
        <i class="ki-duotone ki-down fs-1"></i>
      </div>
    </div>
    <div id="kt_docs_card_collapsible" class="collapse show">
      <div class="card-body">Lorem Ipsum is simply dummy text...</div>
      <div class="card-footer">Footer</div>
    </div>
  </div>
</template>

<script>
export default {
  htmlCode: `<div class="card shadow-sm">
    <div class="card-header collapsible cursor-pointer rotate" data-bs-toggle="collapse" data-bs-target="#kt_docs_card_collapsible">
        <h3 class="card-title">Title</h3>
        <div class="card-toolbar rotate-180">
            <i class="ki-duotone ki-down fs-1"></i>
        </div>
    </div>
    <div id="kt_docs_card_collapsible" class="collapse show">
        <div class="card-body">
            Lorem Ipsum is simply dummy text...
        </div>
        <div class="card-footer">
            Footer
        </div>
    </div>
</div>`,
};
</script>

<style scoped>
/* Add any component-specific styles here */
</style>
