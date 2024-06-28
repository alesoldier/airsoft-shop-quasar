<template>
  <body class="login-container">
    <img src="images/login-page/aksu-img.png" alt="an aks-74u" />
    <img
      src="images/login-page/title-img.png"
      alt="the title of the page : onTarget"
    />

    <h1 class="login-subtitle">LOGIN ACCOUNT</h1>

    <q-card class="q-pa-md row items-start q-gutter-md bg-teal-10">
      <p class="error-label" name="errorLabel">{{ errorText }}</p>
      <div class="form-field">
        <q-input
          v-model="usernameText"
          type="text"
          label="Username:"
          color="black"
        />
      </div>

      <div class="form-field q-py-md">
        <q-input
          v-model="passwordText"
          type="password"
          label="Password:"
          color="black"
        />
      </div>

      <q-btn
        @click="btn"
        type="submit"
        class="q-px-md q-py-md q-mx-auto q-my-md"
        label="Submit"
        color="red-14"
      />
    </q-card>

    <q-card class="q-pa-lg q-my-xl row items-start q-gutter-md bg-teal-10">
      <div class="sign-in-section">
        <img
          class="sing-in-image"
          src="images/login-page/back-jbt.jpeg"
          alt="a soldier holding a customized rifle"
        />
      </div>

      <div class="sign-in-section">
        <text-h3 class="sing-in-title">Don't have an account?</text-h3>
        <text-h5>Don't worry, just</text-h5>
        <q-btn class="q-px-md q-py-md" label="SING UP" color="red-14" />
      </div>
    </q-card>
  </body>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useQuasar } from 'quasar';

const usernameText = ref('');
const passwordText = ref('');
const errorText = document.querySelector('.error-label');
const $q = useQuasar();

function btn() {
  if (usernameText.value == '' || passwordText.value == '') {
    $q.notify('incorrect password or username');
  } else {
    window.location.href = '';
  }
}
</script>
