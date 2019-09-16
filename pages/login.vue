<template>
  <form class="form">
    <v-container class="login-page">
      <v-layout column>
        <v-flex>
          <v-layout>
            <v-flex class="to-come">Войти</v-flex>
            <v-flex class="title-registration">
              <span class="registration-text">
                или
              <nuxt-link to="/registration" class="registration">регистрация</nuxt-link>
              </span>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex>
          <div class="authorization">
            <v-icon class="email-icon">mdi-email</v-icon>
            <input type="email" class="email-field">
          </div>
        </v-flex>
        <v-flex>
          <div class="password">
            <v-icon class="password-icon">mdi-lock</v-icon>
            <input type="password" class="password-field">
          </div>
        </v-flex>
        <v-flex>
          <div class="forgot-section">
            <v-icon class="lock">mdi-lock</v-icon>
            <nuxt-link to="/forgot" class="forgot">Забыли пароль?</nuxt-link>
          </div>
        </v-flex>
        <v-flex>
          <v-layout>
            <v-flex class="checkbox-remember">
              <v-checkbox v-model="disabled" class="checkbox" label="Запомнить" color="red"></v-checkbox>
            </v-flex>
            <v-flex>
              <nuxt-link to="/sfsef">
                <button class="entrance">
                  Войти
                  <v-icon class="entry-right">mdi-arrow-right</v-icon>
                </button>
              </nuxt-link>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
  </form>
</template>

<script>
  export default {
    data() {
      return {
        disabled: true
      }
    }
  }
</script>

<style scoped>
  .login-page {
    width: 410px;
    height: 500px;
  }

  .to-come {
    font-size: 25px;
  }

  .registration {
    color: red;
    text-decoration: none;
  }

  .authorization {
    padding: 10px;
    font-size: 15px;
    font-style: normal;
    border-bottom: 1px solid gray;
  }

  .password {
    padding: 10px;
    font-size: 15px;
    font-style: normal;
    border-bottom: 1px solid gray;
  }

  .forgot {
    color: gray;
    text-decoration: none;
    font-size: 13px;
  }

  .form {
    width: 400px;
    margin: 100px auto 0;
  }

  .title-registration {
    position: relative;
  }

  .registration-text {
    position: absolute;
    bottom: 0;
    right: 0;
    margin-right: -2px;
  }

  .forgot-section {
    text-align: right;
  }

  .entrance {
    background: red;
    border-radius: 3px;
    color: white;
    border: none;
    padding: 1px 9px;
    width: 97px;
    height: 40px;
    margin-left: 157px;
    margin-top: 45px;
    margin-right: -37px;
  }

  .email-field {
    width: 340px;
  }

  .password-field {
    width: 340px;
  }

  .lock {
    color: darkgrey;
    font-size: 15px;
  }

  .email-icon {
    color: darkgrey;
    font-size: 17px
  }

  .entry-right {
    color: white;
  }

  .password-icon {
    color: darkgrey;
    font-size: 17px;
  }

  .checkbox {
    margin-left: 0;
  }
  .checkbox-remember {
    margin-top: 35px;
  }

</style>

<style>
  .checkbox .v-label {
    color: gray;
    font-size: 12px;
  }
</style>