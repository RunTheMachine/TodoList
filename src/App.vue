<template>
  <div id="app" class="container">
    <div class="logo"><i class="fas fa-clipboard-check"></i></div>
    <h1>Ma Todo List</h1>
    <p><i class="fas fa-info-circle"></i> Les messages affichés par défaut non aucune signification car ils proviennent d'une fausse API.</p>
    <todo-list></todo-list>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import TodoList from './components/TodoList'
// index.js or main.js
// index.js or main.js
import 'vuetify/dist/vuetify.min.css' // Ensure you are using css-loader
export default {
  name: 'App',
  components: {
    HelloWorld,
    TodoList,
  }
}
</script>

<style>
*{
  box-sizing:border-box;
}
.container{
  max-width:600px;
  margin:0 auto;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

.logo{
width:100%;
text-align: center;
}

.fa-clipboard-check{
  font-size: 8rem;
  color:#41b883;
}

h1{
  text-align: center;
}

.container > p{
  color: rgb(182, 181, 181);
  margin-top: 3rem;
  font-style: italic;
}

</style>
