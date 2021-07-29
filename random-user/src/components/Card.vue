<template>
  <div class="card"></div>
</template>

<script>
export default {
  name: "Card",
};
</script>

<style lang="scss" scoped>
.card {
  height: 200px;
  width: 150px;
  background-color: rgb(179, 179, 179);
  border-radius: 3px;
  margin-right: 1rem;
  transition: all 200ms ease-in-out;

  &:hover {
    transform: translateY(-3px);
    transition: all 250ms ease-in-out;
    cursor: pointer;
  }
}
</style>
