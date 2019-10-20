<template>
  <div class="hello">
    <hello-dac />
    <hello-neo /> 
  </div>
</template>

<script>
import HelloDac from './HelloDac.vue';
import HelloNeo from './HelloNeo.vue';
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  components: {
    HelloDac,
    HelloNeo
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
