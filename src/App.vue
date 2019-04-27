<template>
  <div id="app" class="container">
    <div class="logo"><i class="fas fa-clipboard-check"></i></div>
    <h1>Ma Todo List</h1>
    <todo-list></todo-list>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import TodoList from './components/TodoList'

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

.fas{
  font-size: 8rem;
  color:#41b883;
}

h1{
  text-align: center;
}

</style>
