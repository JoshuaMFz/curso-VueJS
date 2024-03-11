<template>
  <div>




    <div v-for="obj in todos" v-bind:key="obj.id" class="todos-item">
      {{obj.title}}
    </div>



  </div>
</template>

<script>
  export default {
    name: 'App',
    components: {
    }, data() {
      return {
        todos: [
          {
            "userId": 1,
            "id": 1,
            "title": "delectus aut autem",
            "completed": false
          },
          {
            "userId": 1,
            "id": 2,
            "title": "quis ut nam facilis et officia qui",
            "completed": false
          },
          {
            "userId": 1,
            "id": 3,
            "title": "fugiat veniam minus",
            "completed": false
          },
          {
            "userId": 1,
            "id": 4,
            "title": "et porro tempora",
            "completed": true
          },
          {
            "userId": 1,
            "id": 5,
            "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
            "completed": false
          }
        ]
      }
    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #000;
    margin-left: 60px;
    margin-top: 60px;
  }

  .todos-item {
    background-color: #000;
    color: #fff;
    padding: 3px 5px;
    margin-bottom: 5px;
    max-width: 80%;
  }
</style>