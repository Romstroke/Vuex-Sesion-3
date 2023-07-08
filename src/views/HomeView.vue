<template>
  <div class="home">
    <div class="cabecera">
       <div class="titulo">
          <h1>OpenMusic</h1>
       </div>
    </div>
    <div class="categorias">
        <h2>Categorias</h2>
        <div class="btn_container">
          <button @click="redirectTo('/pop')">Pop</button> <!-- otra forma: @click="$router.push('/pop')" -->
          <button @click="redirectTo('/rock')">Rock</button>
          <button @click="redirectTo('/rap')">Rap</button>
        </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'HomeView',
  components: {
   
  },
  methods:{
    redirectTo(ruta){
      this.$router.push(ruta)
    }
  }
}
</script>

<style scoped>
  .cabecera{
    border: 1px solid black;
    width: 80%;
    margin: 0 auto;
     padding: 1rem;
  }
  .titulo{
    background: gray;
     padding: 2rem;
  }
  .btn_container{
    display: flex;
    width: 50%;
    margin: 0 auto;
    gap: 2px;
  }
  button{
    flex-grow: 1;
    border: none;
    background: green;
    border-radius: 6px;
    padding: 10px;
    color: whitesmoke;
  }

</style>
