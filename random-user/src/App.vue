<template>
  <div class="container">
    <Card
      v-for="person in people"
      :firstName="person.firstName"
      :lastName="person.lastName"
      :gender="person.gender"
      :image="person.image"
    />
    <!-- <Card />
    <Card /> -->
  </div>
  <Button @click="generateCards" v-on:handle-click="randomText"
    >Generate Users</Button
  >
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Card from "./components/Card.vue";
import Button from "./components/Button.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Card,
    Button,
  },
  data: function () {
    return {
      people: [],
    };
  },
  methods: {
    randomText: function () {
      console.log("randomText fn was ran");
    },
    generateUser: async function () {
      let people = this.people;

      const res = await fetch("https://randomuser.me/api");
      let person = {};
      let data = await res.json();

      person.firstName = data.results[0].name.first;
      person.lastName = data.results[0].name.last;
      person.gender = data.results[0].gender;
      person.image = data.results[0].picture.large;

      people.push(person);
    },

    generateCards: async function () {
      if (this.people.length > 0) {
        this.people = [];
      }

      for (let i = 0; i < 3; i++) {
        this.generateUser();
      }

      console.log(this.people);
    },
  },
  mounted: async function () {
    this.generateCards();
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  display: flex;
  justify-content: center;
  margin-bottom: 2rem;
}
</style>
