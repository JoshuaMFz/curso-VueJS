<template>
  <div>
    <button @click.once="onClick">
      Enviar
    </button>

    <div @mouseover.once="onMouseOver" @mouseout.once="onMouseOut">
      Mouse Over
    </div>


    <form action="google.com.br" @submit.prevent="onSubmit" target="_blank">
      <input @keyup="onKeyUp" type="text">
      <button>Enviar</button>
    </form>

  </div>
</template>

<script>
  export default {
    name: 'App',
    components: {
    }, data() {
      return {
      }
    },
    methods: {
      onClick($evt) {
        console.log("click", $evt)
      }, onMouseOver($evt) { console.log("mouseOver", $evt) }, onMouseOut($evt) { console.log("MouseOut", $evt) }, onSubmit($evt) { console.log("submit", $evt) }, onKeyUp($evt) { console.log("KeyUp"), $evt }
    }
  } </script>

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