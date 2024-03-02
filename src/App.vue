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
        <p class="numero_contador"> {{ contador }}</p>
        <button @click="contador--">-</button>
      </div>
      <div id="zerar">
        <button class="zerar" @click="contador = 0">reiniciar</button>
      </div>
      <div class="div1" v-if="contador > 10">
        <h1>O valor do contador é maior que 10!</h1>
      </div>
      <div class="div2" v-if="contador < 10">
        <h1>O valor do contador é menor que 10!</h1>
      </div>
    </div>
    <div class="container2">
        <h1>Exemplo 1 - Mostrando informações na tela</h1>
        <div class="info">
        <p>Nome: {{ nome }} </p>
        <p>O nome tem {{ nome.length }} caracteres</p>
        <p>O nome invertido é: {{ inverter(nome.toUpperCase()) }} </p>
        <hr>
        <p>Idade: {{ idade }} anos</p>
        <p>Para completar 50 anos faltam: {{ 50 - idade }} anos</p>
        <hr>
        <p> Exemplo de saudação usando função: {{ saudacao() }} </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.tudo {
  display: flex;
  flex-direction: row;
}

.container1 {
  background-color: rgb(35, 36, 35);
 margin: 50px;
 border-radius: 15px;
 padding: 50px;
  display: grid;
  align-content: center;
  justify-content: space-evenly;
}

.container2 {
  background-color: rgb(111, 135, 241);
  margin: 50px;
  padding: 50px;
 border-radius: 15px;
  display: grid;
  align-content: center;
  justify-content: space-evenly;
}
p{
  margin:20px 10px;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-weight: 500;
}
button {
  background-color: aliceblue;
  color: rgb(212, 62, 119);
  border-radius: 8px;
  border: 2px solid rgb(240, 221, 228);;
  margin: 5px;
  width: 100px;
  height: 80px;
  font-size: xx-large;
  font-family:Arial, Helvetica, sans-serif;
}

#zerar {
  display: flex;
  align-items: center;
  justify-content: center;
}
.zerar{
  width: 240px;
  height: 50px;
  background: rgb(212, 51, 113);
  font-size: larger;
  font-weight: bold;
  color: aliceblue;
}
.numero_contador{
  font-size: xx-large;
  margin: 7px;
  color:rgb(212, 62, 119) ;
}
/*.info {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}*/

h1 {
  color: aliceblue;
  font-weight: bold;
  font-size: large;
  font-family:Arial, Helvetica, sans-serif;
  text-align: center;

}

.div1,
.div2 {
  margin: 30px;
  display: block;
}

.div1>h1 {
  color:rgb(212, 62, 119);;
}

.div2>h1 {
  color: rgb(255, 255, 255);
}
.contador,
.div1,
.div2 {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>