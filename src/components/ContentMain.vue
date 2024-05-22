<template>
  <section class="section-advice">
    <div class="advice-container">
      <p v-if="conselho">{{ conselho }}</p>
      <div v-else>
        <p>Nothing yet...</p>
      </div>
    </div>
    <button class="btn-generator" @click="getPhrase">Get advice</button>
  </section>
</template>

<script>
  import axios from 'axios';

  export default {
    data() {
      return {
        conselho: ''
      };
    },
    methods: {
      getPhrase() {
        axios.get('https://api.adviceslip.com/advice')
          .then(response => {
            this.conselho = response.data.slip.advice;
          })
          .catch(error => {
            console.error(error);
          });
      }
    }
  }
</script>

<style>
  .section-advice {
    display: flex;
    flex-flow: column;
    gap: 2vh;

    padding: 15vh 0;
  }

  .advice-container {
    text-align: center;
    font-size: 1.5rem;
    padding: 5vw;
  }

  .advice-container p {
    transition: 2s;
  }

  .btn-generator {
    padding: 1rem;

    font-size: 1rem;
    color: #002F50;
    border: none;
    border-radius: 10px;
    transition: 0.5s;
    cursor: pointer;
  }

  .btn-generator:hover {
    color: green;
    transform: translate(-5px, -5px);
  }

  .btn-generator:active {
    color: green;
  }
</style>
