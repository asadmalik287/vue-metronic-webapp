<!-- HeaderComponent.vue -->

<template>
  <div class="card shadow-sm">
    <div class="card-header">
      <h3 class="card-title">Fluid Image</h3>
      <div class="card-toolbar">
        <button type="button" class="btn btn-sm btn-light">Action</button>
      </div>
    </div>
    <div class="card-body p-0">
      <div class="card-p mb-10">
        Lorem Ipsum is simply dummy text ...

        <div class="text-center px-4">
          <img
            class="mw-100 mh-300px card-rounded-bottom"
            alt=""
            src="@/assets/images/cardSix.png"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  htmlCode: `<div class="card shadow-sm">
    <div class="card-header">
        <h3 class="card-title">Fluid Image</h3>
        <div class="card-toolbar">
            <button type="button" class="btn btn-sm btn-light">
                Action
            </button>
        </div>
    </div>
    <div class="card-body p-0">
        <div class="card-p mb-10">Lorem Ipsum is simply dummy text ...

        <div class="text-center px-4">
            <img class="mw-100 mh-300px card-rounded-bottom" alt="" src="examples.png"/>
        </div>
    </div>
</div>`,
};
</script>

<style scoped>
/* Add any component-specific styles here */
</style>
