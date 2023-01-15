<template>
  <div class="my-box">
    <slot></slot>
  </div>
</template>

<script>
export default {};
</script>

<style>
.my-box {
  padding: 1rem;
  margin: 1.5rem 0;
  border-radius: 6px;
  box-shadow: 15px 15px 15px rgba(0, 0, 0, 0.15);
  background-color: beige;
}
</style>
