<template>
  <div style="display: flex;">

    <div class="image">

    </div>

    <section class="inputContainer">
      <div class="inputs">
        <img class="logoUnimar" src="../assets/images/logoUnimar.svg" alt="">
        <h1>Fórum de perguntas e respostas</h1>
        <div class="" style="display: flex;flex-direction: column; width: 50%;margin-inline: auto;gap:2rem;">
          <FloatLabel>
            <InputText id="username" v-model="email" />
            <label for="username">E-mail</label>
          </FloatLabel>
          <FloatLabel>
            <Password v-model="senha" toggleMask :feedback="false" inputId="password" />
            <label for="password">Senha</label>
          </FloatLabel>
        </div>
        <Button style="width: 50%; margin-inline: auto"><a href="/Home" class="texto-button-entrar">Entrar</a></Button>
        <a href="/register" style="margin-inline: auto;color: white;">Cadastre-se</a>
      </div>
    </section>
  </div>
</template>

<script setup>

import { ref } from 'vue';

const email = ref(null);
const senha = ref(null);
</script>

<style >
.image {
  width: 70vw;
  height: 100vh;
  background: #2D2D30;
}

.inputContainer {
  width: 30vw;
  height: 100vh;
  background: #252526;
  margin: auto;
}

.logoUnimar {
  width: 5rem;
  margin-inline: auto;
}

.inputs {
  gap: 2.5rem;
  height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: auto;
}

h1 {
  width: 13rem;
  text-align: center;
  margin-inline: auto;
  color: white;
  font-size: large;
  line-break: auto;
}

.p-inputtext{
  width: 100%;
  border-radius: 0rem !important;
  border: none !important;
  border-bottom: white 1px solid !important;
  background-color: #2D2D30 !important;
  color: white !important;
}

.p-password{
  input{

    width: 100%;
  }
  width: 100%;
}

.p-button{
  width: 7rem !important;
  border-radius: 0rem !important;
  background-color: white !important;
  color: #252526 !important;
  border: none !important;

}
</style>