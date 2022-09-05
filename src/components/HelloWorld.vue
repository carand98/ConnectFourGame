<template>
  <div>
    <h2>Player 1</h2>
    <input type="text" placeholder="Username" v-model="query" />

    <button @click="reset">Submit</button>

    <div>
      {{ query }}
    </div>
    
  </div>
</template>

<script>
  import { ref } from 'vue';
export default {
  setup() {
    const query = ref('')

    const reset = () => {
      query.value = ''
    }
    return {
      reset,
      query,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
button {
  margin-left: 5px;
}
</style>
