<template>

  <section class="src-componentes-texto">
    Color: <input type="text" v-model="colorFuente">
    Fondo: <input type="text" v-model="fondoFuente">
    Size:  <input type="text" v-model="sizeFuente">
    
    <br><br><hr><br>
    Texto: <input type="text" v-model="valorTexto" :style="getEstilos()"> 
    <br><br>
    <div v-if="valorTexto.length">Cantidad de palabras: {{calcularPalabras}}</div>
    <h3 v-else> No hay texto escrito </h3><br><br>
    <table class="table">
      <hr>
      <tr>
        <th>Numero de pregunta</th>
        <th>|</th>
        <th>Respuesta</th>
      </tr>
      <hr>
      <tr>
        <th>1</th>
        <th>|</th>
        <th>B</th>
      </tr>
      <hr>
      <tr>
        <th>2</th>
        <th>|</th>
        <th>B</th>
      </tr>
      <hr>
      <tr>
        <th>3</th>
        <th>|</th>
        <th>C,D</th>
      </tr>
      <hr>
      <tr>
        <th>4</th>
        <th>|</th>
        <th>D</th>
      </tr>
      <hr>
      <tr>
        <th>5</th>
        <th>|</th>
        <th>B,D</th>
      </tr>
      <hr>
    </table>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-componentes-texto',
    props: [],
    mounted () {

    },
    data () {
      return {
        valorTexto: 'Hola Mundo',
        colorFuente: 'black',
        fondoFuente: 'white',
        sizeFuente: '10px',
      }
    },
    methods: {
      getEstilos(){
        return {
          color: this.colorFuente,
          backgroundColor: this.fondoFuente,
          fontSize: this.sizeFuente,
        }
      }
    },
    computed: {
        calcularPalabras(){
        let texto = this.valorTexto.split(' ')
        console.log(texto)
        return texto.length
      },
    }
}


</script>

<style scoped lang="css">
  .src-componentes-texto {

  }
</style>
