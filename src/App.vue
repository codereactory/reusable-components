<template>
  <div id="app">
    <h1>Reusable Components</h1>
    <section>
      <ul>
        <li v-for="x in 6" :key="x">
          <c-heading :level="x">Heading {{ x }}</c-heading>
        </li>
      </ul>
    </section>
    <section>
      <ul>
        <li v-for="x in 6" :key="x">
          <c-heading :level="x" :as="6">Heading {{ x }}</c-heading>
        </li>
      </ul>
    </section>
    <section>
      <c-heading level="6" as="1" large>Big Heading</c-heading>
    </section>
  </div>
</template>

<script>
import CHeading from './components/CHeading.vue'
export default {
  name: 'app',
  components: {
    CHeading,
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

ul {
  list-style: none;
  text-align: left;
}
</style>
