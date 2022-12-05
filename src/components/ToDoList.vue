<template>

  <input type="text" v-model='todo' @change="addItem(todo)" placeholder="Új feladat megadása">

  <!-- <ul>
    <li v-for="needtodo in todoList">
    {{needtodo}}
    </li>
  </ul> -->

  <table>
    <tr v-for="todoN in todoList">
    <td> {{todoN}} </td>
    <td>  <span class="btn btn-danger" @click="deleteItem(todo)"> Törlés </span></td>
  </tr>
  </table>

</template>
<script setup>

import {ref} from 'vue';
const todo = ref('');
const todoList = ref([]);

function addItem(t){
  todoList.value.push(t);
  todo.value = '';
}

</script>
<style scoped>
  
</style>