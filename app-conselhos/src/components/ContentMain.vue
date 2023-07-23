<template>
    <div class="main">
        <div class="conselho">
            <p id="resultado"></p>
        </div>
        <button id="btnGerarConselho">Nova Frase</button>
    </div>
</template>

<style>
.main {
    width: 100%;
    height: 100%;
}
.conselho {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 10%;
    width: 75%;
    background-color: #002f40dc;
    color: #ececec;
    font-size: larger;
    font-family: 'Times New Roman', Times, serif, Arial, Helvetica, sans-serif;
    font-style: italic;
    border-radius: 10px;
    box-shadow: 5px 10px 25px 0px rgba(0,0,0,0.75);
    -webkit-box-shadow: 5px 10px 25px 0px rgba(0,0,0,0.75);
    -moz-box-shadow: 5px 10px 25px 0px rgba(0,0,0,0.75);
}
</style>

<script>
import axios from 'axios';
    // Função para fazer a requisição usando Axios
    function obterConselhoAleatorio() {
      axios.get('https://api.adviceslip.com/advice')
        .then(function (response) {
          const conselho = response.data.slip.advice;
          console.log(conselho);
          const divResultado = document.getElementById("resultado");
          divResultado.innerText = conselho;
        })
        .catch(function (error) {
          console.error(error);
        });
    }
    document.addEventListener("DOMContentLoaded", function () {
        const btnGerarConselho = document.getElementById("btnGerarConselho");
        btnGerarConselho.addEventListener("click", obterConselhoAleatorio);
    });
</script>