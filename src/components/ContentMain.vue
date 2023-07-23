<template>
    <div class="main">
        <div class="conselho">
            <p id="resultado"></p>
        </div>
        <button class="btn" id="btnGerarConselho">Nova Frase</button>
    </div>
</template>

<style>
.main {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
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
    margin-bottom: 3%;
}
/* Botão */
.btn {
 width: 10%;
 height: 5%;
 font-size: 1.1em;
 cursor: pointer;
 background-color: #00a6ff;
 color: #fff;
 border: none;
 border-radius: 5px;
 transition: all .4s;
 font-family: 'Raleway', Times, serif, Arial, Helvetica, sans-serif;
}

.btn:hover {
 border-radius: 5px;
 transform: translateY(-10px);
 box-shadow: 0 7px 0 -2px #39a2dbab,
  0 15px 0 -4px #bce7ff,
  0 16px 10px -3px #39a2db;
}

.btn:active {
 transition: all 0.2s;
 transform: translateY(-5px);
 box-shadow: 0 2px 0 -2px #002f40dc,
  0 8px 0 -4px #39a2db,
  0 12px 10px -3px #39a2db;
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