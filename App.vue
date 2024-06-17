<script>
export default {
  data() {
    return {
      valor1:"",
      valor2:"",
      nameSoft: "Calculadora",
      label1: "Valor 1",
      label2: "Valor 2",
      resultadoSuma: "",
      resultadoResta: "",
      resultadoMultipli: "",
      resultadoDivi: "",
    };
  },
  methods: {
    sumar() {
      this.resultadoSuma = parseInt(this.valor1) + parseInt(this.valor2);
      this.resultadoResta = "";
      this.resultadoMulti = "";
      this.resultadoDivi = "";
    },
      restar() {
      this.resultadoResta = parseInt(this.valor1) - parseInt(this.valor2);
      this.resultadoSuma = "";
      this.resultadoMulti = "";
      this.resultadoDivi = "";
    }, 
    Mult() {
      this.resultadoMulti = parseInt(this.valor1) * parseInt(this.valor2);
      this.resultadoSuma = "";
      this.resultadoResta = "";
      this.resultadoDivi = "";
    },
    Divi() {
        this.resultadoDivi = parseInt(this.valor1) / parseInt(this.valor2);
        this.resultadoResta = "";
        this.resultadoMulti = "";
        this.resultadoSuma = "";
    },
  }
}; 
</script>
<template>
  <div>
    <h2>{{ nameSoft }}</h2>
    <label>{{ label1 }}</label>
    <input type="text" v-model="valor1" placeholder="Ingresa el valor 1"> <br>
    <label>{{ label2 }}</label>
    <input type="text" v-model="valor2" placeholder="Ingresa el valor 2"> <br>  
    <button @click="sumar">Sumar</button>
    <button @click="restar">Restar</button>
    <button @click="Mult">Multiplicar</button>
    <button @click="Divi">Dividir</button> <br>  
    <span v-if="resultadoSuma !== ''" >La suma de {{ valor1 }} mas {{ valor2 }} es igual a {{ resultadoSuma }}. </span>
    <span v-if="resultadoResta !== ''">La resta de {{ valor1 }} menos {{ valor2 }} es igual a {{ resultadoResta }}. </span>
    <span v-if="resultadoMulti !== ''">La multiplicacion de {{ valor1 }} y {{ valor2 }} es igual a {{ resultadoMulti }}. </span>
    <span v-if="resultadoDivi !== ''">La division de {{ valor1 }} y {{ valor2 }} es igual a {{ resultadoDivi }}. </span>
  </div>
</template>
<style scoped>
div {
backgroud-color: black;
}
</style>
