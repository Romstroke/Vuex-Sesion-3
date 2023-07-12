<template>
    <div>
        <h2>Agregar Nuevo Album</h2>
        <form>
            <label for="">Artista</label>
            <input v-model="album.artist" type="text">

            <label for="">Album</label>
            <input  v-model="album.album" type="text">

            <label for="">Portada</label>
            <input v-model="album.image" type="text">

            <label for="">Genero</label>
            <select v-model="album.category"> 
                <option value="rock">rock</option>
                <option value="rap">rap</option>
                <option value="pop">pop</option>
            </select>

            <div>
                <button  @click.prevent="agregar" >Agregar Album</button>
            </div>
        </form>
    </div>
</template>

<script>

import {mapActions} from 'vuex'

export default {
    name: 'Album-Add',
  
    // props: {},
    data: function(){
        return {
            album:{
                artist:'',
                album:'',
                image:'',
                category:'',

             }
        }
    },
    // computed: {},
    methods: {
        ...mapActions(['add_album']),
        agregar(){
            //validar
            //let category = this.album.category
            this.album.id = Math.floor(Math.random()*1000)
            this.add_album({...this.album})
            //this.$router.push(`/${category}`)
        }
    }
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
    
</style>