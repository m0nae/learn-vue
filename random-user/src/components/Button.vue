<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
button {
  cursor: pointer;
  padding: 1rem 2rem;
  background-color: tomato;
  border: none;
  border-radius: 3px;
  color: white;
  font-weight: 600;
  font-size: 1rem;
}
</style>
