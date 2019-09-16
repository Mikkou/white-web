<template>
  <v-app>
    <div class="header">
      <nuxt-link class="link-logo" to="/">
        <div class="logo"> м</div>
      </nuxt-link>
      <div>
        <nuxt-link class="registration" to="/registration">
          <button class="button-registration">
            <div class="logo-registration">
              <span>м</span>
            </div>
            <div class="registration">
              Регистрация
            </div>
          </button>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/login">
          <button class="entrance"> Войти</button>
        </nuxt-link>
      </div>
    </div>
    <nuxt/>
  </v-app>
</template>

<style>
  .logo-registration {
    font-size: 10px;
    padding: 4px;
    width: 20px;
    height: 20px;
    background: white;
    color: red;
    border: none;
    border-radius: 50%;
    margin-left: 5px;
    margin-top: 3px;
    text-decoration: none;
  }

  .link-logo {
    text-decoration: none;
  }

  .registration {
    margin-left: 5px;
    padding: 2px 5px;
    border-radius: 5px;
    text-decoration: none;
  }

  .button-registration {
    display: inline-flex;
    color: white;
    margin-left: 1200px;
    margin-top: 7px;
    background: red;
    padding: 1px 7px;
    border-radius: 5px;
    border: none;
    height: 27px;
  }

  .entrance {
    margin-left: 20px;
    margin-top: 7px;
    padding: 1px 9px;
    border: 1px solid black;
    border-radius: 5px;
    height: 26px;
    color: black;
  }

  .header {
    display: inline-flex;
    background: #eaeaea;
    height: 40px;
    width: 100%;
  }

  .logo {
    width: 28px;
    background: red;
    color: white;
    border: none;
    border-radius: 50%;
    margin-left: 5px;
    padding: 1px 8px;
    height: 28px;
    margin-top: 5px;
    text-decoration: none;
  }
</style>

