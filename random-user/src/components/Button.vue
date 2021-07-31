<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "Button",
  methods: {
    handleClick() {
      this.$emit("handle-click");
    },
  },
};
</script>

<style lang="scss" scoped>
button {
  cursor: pointer;
  padding: 1rem 2rem;
  background-color: rgb(161, 76, 231);
  border: none;
  border-radius: 3px;
  color: white;
  font-weight: 600;
  font-size: 1rem;

  &:hover {
    background-color: rgb(148, 69, 212);
  }
}
</style>
