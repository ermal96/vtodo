<template>
  <div class="todos" :key="todo.id" v-for="todo in todos">
   <Todo :id="todo.id" :name="todo.name" :status="todo.status" />
  </div>
</template>


<script>
// @ is an alias to /src
import {mapGetters} from 'vuex';
import Todo from '../components/Todo/index';
export default {
  name: 'Todos',
  computed: {
    ...mapGetters({todos: 'getTodos'}),
  }, 
 
  components: {
    'Todo': Todo
  },
}
</script>


