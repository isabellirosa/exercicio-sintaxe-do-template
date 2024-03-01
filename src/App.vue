<script setup>
import { ref } from "vue"
const nome = 'Isabelli'
const idade = 16
const contador = ref(0);

function inverter(texto) {
  return texto.split('').reverse().join('')
}

function saudacao() {
  return `Olá, ${nome}!`
}
</script>
/* export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador(){
    if(this.contador>0)this.contador--
    },
    zerar(){
    this.contador=0
    }
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
 }
<!-- </script> -->

<template>
  <div class="tudo">
  <div class="container1">
    <div class="contador">
      <button @click="contador++">+</button>
      <p> {{ contador }}</p>
      <button @click="contador--">-</button>
      <button id="zerar" @click="contador = 0">Zerar</button>
    </div>
    <div class="div1" v-if="contador > 10">
      <h1>O valor do contador é maior que 10!</h1>
    </div>
    <div class="div2" v-if="contador < 10">
      <h1>O valor do contador é menor que 10!</h1>
    </div>
  </div>
  <div class="container2">
    <div class="info">
      <h1>Exemplo 1 - Mostrando informações na tela</h1>
      <p>Nome: {{ nome }} </p>
      <p>Idade: {{ idade }} anos</p>
      <hr />
      <p>Para completar 50 anos faltam: {{ 50 - idade }} anos</p>
      <p>O nome tem {{ nome.length }} caracteres</p>
      <p>O nome invertido é: {{ inverter(nome.toUpperCase()) }} </p>
      <hr />
      <p> Exemplo de saudação usando função</p>
      <p> {{ saudacao() }} </p>
    </div>
  </div>
</div>
</template>

<style scoped>
.tudo{
  display:flex;
  flex-direction: row;
}
.container1{
  background-color: rgb(201, 201, 86);
  width: 50%;
  height: 700px;
  display: grid;
  align-content: center;
  justify-content: space-evenly;
}
.container2{
  background-color: rgb(119, 201, 86);
  width: 50%;
  height: 700px;
}
button {
  background-color: rgb(231, 230, 255);
  border-radius: 8px;
  border: 1px solid black;
  margin: 5px;
  width:50px;
  height: 50px;
}
#zerar{
  width:150px;
  display:block;
}
/*.info {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}*/

h1 {
  color: rgb(255, 255, 255);
  font-weight: bold;
  font-size: 1.5em;

}

.div1,
.div2 {
  margin: 30px;
  display: block;
}

.div1>h1 {
  color: green;
}

.div2>h1 {
  color: rgb(255, 48, 48);
}

.contador,
.div1,
.div2 {
  display: flex;
  align-items: center;
  justify-content: center;
}</style>