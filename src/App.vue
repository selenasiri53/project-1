<template>
  <section>
    <!-- 1) Output your name -->
    <h2>{{ name }}</h2>
    <!-- 2) Output your age -->
    <p>{{ age }}</p>
    <!-- 3) Output your age + 5 -->
    <p>{{ calculateAge() }} in 5 years</p>
    <!-- 4) Output a random number (0 to 1) -->
    <p>Favorite Number: {{ generateRandomNumber() }}</p>
    <div>
      <!-- 5) Display some image you found via Google -->
      <!-- <img src="SOME IMAGE URL" /> -->
      <img v-bind:src="imageUrl" style="width: 25%; height: 25%" />
    </div>
    <!-- 6) Prepopulate the input field with your name via the "value" attribute -->
    <input type="text" :value="name" />
  </section>
</template>

<script>
export default {
  name: 'App',
  components: {},
  data() {
    return {
      enteredValue: '',
      name: 'Selena',
      age: 25,
      imageUrl:
        'https://images.pexels.com/photos/11346010/pexels-photo-11346010.jpeg?cs=srgb&dl=pexels-justyna-serafin-11346010.jpg&fm=jpg&_gl=1*4cy3rr*_ga*ODg4Njc2NDk2LjE2NjY2NzI2NzY.*_ga_8JE65Q40S6*MTY2Nzk1ODAzNS4yLjEuMTY2Nzk1ODI0Ni4wLjAuMA..',
    };
  },
  methods: {
    calculateAge() {
      return this.age + 5;
    },
    generateRandomNumber() {
      return Math.random();
    },
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
}
</style>
