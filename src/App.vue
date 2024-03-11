<template>
  <div>
    One-Way Data Binding
    Two-Way Data Binding
    V-Model -> Formulários
    <br><br><br>
    <div>
      <label>Nome</label> <br>
      <input v-model="name" type="text"> <br><br>
      {{ name }}
    </div>

    <div>
      <br><br><br>
      <label>Sports</label> <br>
      <select v-model="sports">
        <option value=''>Escolha</option>
        <option value="skate">Skate</option>
        <option value="futebol">Futebol</option>
        <option value="tenis">Tenis</option>
        <option value="fonfon">Birifonnn</option>
      </select>
      {{ sports }}
    </div>


    <br><br><br>

    <div>
      <label>Newsletter</label> <br>
      <input v-model="newsletter" type="radio" value="Sim"> Sim <br>
      <input v-model="newsletter" type="radio" value="Não"> Não <br>
      {{ newsletter }}
    </div>

    <br><br><br>

    <div>
      <label>Contrato</label> <br>
      <input v-model="contract" type="checkbox"> Aceita nosso contrato? <br>
      {{ contract }}
    </div>

    <br><br><br>

    <div>
      <label>Cores</label> <br>
      <input v-model="colors" type="checkbox" value="Amarelo"> Amarelo <br>
      <input v-model="colors" type="checkbox" value="Azul"> Azul <br>
      {{ colors }}
    </div>

  </div>
</template>

<script>
  export default {
    name: 'App',
    components: {
    }, data() {
      return {
        name: "Jon Snow",
        sports: '',
        newsletter: '',
        contract: '',
        colors: [],
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
</style>