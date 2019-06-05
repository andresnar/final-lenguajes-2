<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span class="font-weight-light">CUIDA A TUS FAMILIARES CON ALZHEIMER</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        flat
        href="https://www.alz.org/"
        target="_blank"
      >
        <span class="mr-2">Mas Informacion</span>
      </v-btn>
    </v-toolbar>
    

    <v-content>
      <barra/>
      <hr>
    </v-content>


    <v-conteiner aling="center">
      <v-layout test-xs-center wrap>
      <Carrusel/><br>
      </v-layout>
      <h1 id="titulo1" align="center"><u>Amar Sin Condición</u></h1>

      <v-tabs v-model="active" color="cyan" dark slider-color="yellow">
        <v-tab ></v-tab>
      </v-tabs>
      <v-layout text-xs-center wrap>  
      <iframe width="1150" height="550" src="https://www.youtube.com/embed/UkviIKg0-5k" frameborder="0" 
          allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
      </iframe>
      </v-layout>
    </v-conteiner>

    <v-content>
      <pagina/>
      <Footer/>
    </v-content>
    
  </v-app>
</template>

<script>
import barra from './components/barra'
import pagina from './components/Pagina'
import Footer from './components/footer'
import Carrusel from './components/carruser'

export default {
  name: 'App',
  components: {
    pagina, barra, Footer, Carrusel
  },
  data () {
    return {
      //
    }
  }
}
</script>

<style>
  #titulo1{
        font: oblique bold cursive;
        font-size:30px;
        text-shadow: 3px 2px lightgray;}
  
</style>
