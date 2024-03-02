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
function incrementar() {
    contador.value++;
  }

  function decrementar() {
    if (contador.value > 0) {
      contador.value--;
    }
  }
</script>

<template>
  <div class="tudo">
    <div class="container1">
      <div class="contador">
        <button @click="incrementar">+</button>
        <p class="numero_contador"> {{ contador }}</p>
        <button @click="decrementar">-</button>
      </div>
      <div id="zerar">
        <button class="zerar" @click="contador = 0">reiniciar</button>
      </div>
      <div class="maior-ou-menor">
        <p v-if="contador > 10" class=maior>O valor do contador é maior que 10!</p>
        <p v-else-if="contador < 10" class="menor">O valor do contador é menor que 10!</p>
        <p v-else class="igual">O valor do contador é igual a 10!</p>
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
  height: min-content;
 margin: 50px;
 border-radius: 15px;
 padding: 50px;
  display: grid;
  align-content: center;
  justify-content: space-evenly;
}

.container2 {
  background-color: rgb(111, 135, 241);
  height: min-content;
  margin: 50px;
  padding: 50px;
 border-radius: 15px;
  display: grid;
  align-content: center;
  justify-content: space-evenly;
}
p{
  margin:10px 0px;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-weight: 100;
  color: rgb(31, 34, 37);
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
h1 {
  color: aliceblue;
  font-weight: bold;
  font-size: large;
  font-family:Arial, Helvetica, sans-serif;
  text-align: center;

}
.maior {
  color:rgb(212, 62, 119);
  font-weight: bold;
}

.menor {
  color: rgb(255, 255, 255);
  font-weight: bold;
}
.igual{
  color: rgb(63, 167, 49);
  font-weight: bold;
}
.contador{
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>