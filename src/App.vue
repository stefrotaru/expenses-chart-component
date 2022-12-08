<template>
  <!-- <div class="container"> -->
    <ExpensesApp/>
  <!-- </div> -->
</template>

<script>
import ExpensesApp from './components/ExpensesApp.vue';

export default {
  name: 'App',
  components: {
    ExpensesApp
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;700&display=swap');

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {}

body {
  height: 100vh;
  background-color: #2c3e50;
  font-family: 'DM Sans', sans-serif;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: white;
  margin-top: 60px;

  max-width: 600px;
}
</style>
