<template>
    <div>
        <v-flex>
          <v-text-field
            placeholder="Penser à ..."
            class="todo-input"
            v-model="newTodo" @keyup.enter="addTodo"
          ></v-text-field>
        </v-flex>
      <div v-for="(todo, index) in todos" :keys="todo.id" class="todo-item">  
          <div>
            {{todo.title}} 
          </div>
          <div class="remove-item" @click="removeTodo(index)">
            X
          </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'todo-list',
  data () {
    return {
      newTodo: '',
      idForTodo: 3,
      todos:[
        {
          'id': 1,
          'title': 'Acheter du lait',
          'completed' : false,
        },
        {
          'id': 2,
          'title': 'Rendre le livre à la bibliothèque',
          'completed' : false,
        },
      ]
    }
  },
  methods:{
    addTodo(){
      if(this.newTodo.trim().length == 0){
        return
      }
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed:false,
      })

      this.newTodo = ''
      this.idForTodo++
    },
    removeTodo(index){
      this.todos.splice(index,1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.todo-input{
  width:100%;
  padding: 10px 18px;
  font-size: 18px;
  margin-bottom:16px;
}

.todo-item{
  margin-bottom:12px;
  display:flex;
  align-items:center;
  justify-content: space-between;
  background-color:#34495e;
  padding:10px;
  color:#fff;
  border-radius: 5px;
}

.remove-item{
  cursor: pointer;

}

</style>
