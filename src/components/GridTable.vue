<template>
  <div class="Connec4Layout">
    <table ref="table">
      <thead>
        <th v-for="cell in columns" :key="cell">
          <span v-if="cell == 1"> Player 1</span>
          <span v-if="cell == 6"> Player 2</span>
        </th>
      </thead>
      <tbody>
        <tr v-for="row in rows" :key="row">
          <td v-for="body_cell in columns" :key="body_cell"> {{ body_cell }}</td>
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
/*  th{
    padding: 5px;
  }
*/
/* td {
  padding: 2.5px;
  width: calc(100% / 6);
} */

#Connect4Layout {
  margin: 20px 0;
}
#Connect4Layout table {
  min-width: 300px;
  width: 100%;
  height: fit-content;
  overflow-y: scroll;
  border-collapse: collapse;
  border: 1px solid #000;
}
#Connect4Layout table tr td {
  border: 1px solid #000;
  padding: 10px;
}
#Connect4Layout table .bold {
  border-right: none;
  border-left: none;
  background: #ddd;
  border-bottom: 1px solid #c2c2c2;
  border: none;
}
#Connect4Layout table .bold td {
  border: none;
  background: #000;
  color: #fff;
  border: none;
  font-size: 18px;
  font-weight: bold;
}
#Connect4Layout .with-header tr:first-of-type td {
  border: none;
}
@media (max-width: 480px) {
  #Connect4Layout .with-header tr:first-of-type {
    display: none;
  }
  #Connect4Layout .with-header tr {
    border: 1px solid #000;
  }
  #Connect4Layout .with-header tr td {
    display: block;
    border: none;
  }
  #Connect4Layout .with-header tr td:first-child {
    padding-top: 0.5em;
  }
  #Connect4Layout .with-header tr td:last-child {
    padding-bottom: 0.5em;
  }
  #Connect4Layout .with-header tr td:before {
    content: attr(data-th) " : ";
    font-weight: bold;
    display: inline-block;
  }
}
@media (max-width: 480px) and (min-width: 480px) {
  #Connect4Layout .with-header tr td:before {
    display: none;
  }
}
</style>
