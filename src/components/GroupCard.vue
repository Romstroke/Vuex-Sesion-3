<template>
        <div class="card_container">
            <div class="card" v-for="album in musicgenre" :key="album.id">
                <h2>{{album.artist}}</h2>
                <img :src="album.image" alt="" srcset="" width='80%' >
                <h3>{{album.album}}</h3>
            </div>
        </div>
</template>

<script>
export default {
    name: 'group-card',
    props: {
        musicgenre:{
            type:Array,
            required:true
        }
    },
    data: function(){
        return {}
    },
    // computed: {},
    //methods: {}
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
        .card_container{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        width: 70%;
        margin: 0 auto;
        gap:10px;
    }
    .card{
        padding: 20px;
         border: none;
        box-shadow:       
        inset 0 -3em 3em rgba(0,0,0,0.1),             
        /* 0 0  0 2px rgb(255,255,255),              */
        0.3em 0.3em 1em rgba(0,0,0,0.3);
       
    }
</style>