<template>
  <div class="card">
  <img :src="image" alt="person" />
    <p>{{firstName}} {{lastName}}</p>
    <p>{{ gender }}</p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ['firstName', 'lastName', 'gender', 'image']
  
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

  img {
    border-radius: 50%;
    height: 40%;
    width: auto;
    margin-top: 0.5rem;
  }
}
</style>
