<template>
  <div>
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
* {
  margin-top: 100px;
}
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
