<template>
  <div class="Connec4Layout">
    <table ref="table">
      <tbody>
        <tr v-for="row in rows" :key="row">
          <td v-for="body_cell in columns" :key="body_cell"></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
import { ref } from "vue";

const table = ref("null");

const columns = 6;

const rows = 7;
</script>

<style>

#Connec4Layout {
  
}
table {
  margin: auto;
  background-color: blueviolet;
  display: flex;
  flex-direction: column;
  max-width: 350px;
  gap: 5px;
}

tbody {
  display: flex;
  flex-direction: column;
  align-items: center;
}

td {
  background-color: white;
  padding: 2.5px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
}
</style>
