<template>
  <div>
    <h1 :class="{ 'title': false, 'title-home': isHome }">
      Curso Vue 3
    </h1>

    <p :class="pClass">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Debitis ducimus cupiditate, id repudiandae consequatur
      quisquam esse laborum ex placeat nisi non, eveniet atque maiores voluptatibus aspernatur ad. Libero, alias ut?
    </p>

    <p :style="classStyle">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam deleniti molestiae tenetur illum nulla nihil eum
      quidem repellendus recusandae, aut quaerat asperiores sint accusamus, officia ipsum debitis et modi assumenda?
    </p>


    <div v-for="(obj, index) in todos" v-bind:key="obj.id" class="todos-item">
      <img :src="obj.SrcAlt" v-if="obj.SrcAlt">
      {{index }} - {{obj.title}}
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
            "completed": false,
            "SrcAlt": "https://placehold.co/600x400"
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
        ],
        classVar: 'title',
        isHome: true,
        pClass: ['text', 'text-home'],
        classStyle: { color: 'green', backgroundColor: 'black', 'font-size': '3rem' }
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

  .title {
    font-size: 2.5rem;
    color: blue;
  }

  .title-home {
    font-size: 3rem;
    color: green;
  }

  .text-home {
    font-size: 2rem;
    color: aqua;

  }
</style>