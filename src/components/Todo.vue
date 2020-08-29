<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
  <div>
    <input type="text" placeholder="Add todo here" class="input" v-model="newTodo" @keyup.enter="addTodo()" />
  </div>
  <div class="todo-list-box">
    <p class="todo-list-title">List Todo :</p>
    <div class="todo-list-job" v-for="(todoList, index) in todoLists" :key="todoList.id">

      <hr>
      {{todoList.title}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      newTodo: '',
      idForTodo: 3,
      todoLists: 
        [
          {
            id: 1,
            title: 'Going Cook',
            completed: false,
          },
          {
            id: 2,
            title: 'Going Wash',
            completed: false,
          }
        ],
    }
  },
  methods: {
    addTodo() {
      this.todoLists.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false,
      });
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.input {
  width: 94%;
  padding: 12px 10px;
  font-size: 20px;
  color: rgb(82, 81, 81);

  &:focus{
    outline: 0;
  }
}

.todo-list-box {
  padding: 5px 10px;
  font-size: 16px;
  text-align:left;
  margin-top:20px;
  -webkit-box-shadow: 10px 10px 33px 9px rgba(0,0,0,0.35);
  -moz-box-shadow: 10px 10px 33px 9px rgba(0,0,0,0.35);
  box-shadow: 0px 0px 5px 5px rgba(223, 222, 222, 0.35);
}
.todo-list-title {
  font-size: 14px;
}
.todo-list-job {
  margin-top: 10px;
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
</style>
