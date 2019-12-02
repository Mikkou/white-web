<template>
  <v-container
    class="fill-height"
    fluid
  >
    <v-row
      align="center"
      justify="center"
    >
      <v-col
        class="registration"
      >
        <v-card
          class="elevation-0 transparent"
        >
          <v-form
            ref="form"
            v-model="valid"
            lazy-validation
          >
            <v-toolbar
              color="transparent"
              dark
              flat
            >
              <v-toolbar-title class="registration__title">Создать учётную запись</v-toolbar-title>
            </v-toolbar>
            <v-card-text class="input-default">
              <v-row
                align="center"
                justify="center"
              >
                <v-col
                  xs="6"
                  class="pr-0 py-0"
                >
                  <v-text-field
                    v-model="firstname"
                    :rules="[required]"
                    label="Имя"
                    name="name"
                    color="#757575"
                    prepend-inner-icon="mdi-account-outline"
                    type="text"
                    required
                  />
                </v-col>
                <v-col
                  xs="6"
                  class="pl-0 py-0"
                >
                  <v-text-field
                    v-model="lastname"
                    :rules="[required]"
                    label="Фамилия"
                    name="lastname"
                    color="#757575"
                    type="text"
                    required
                  />
                </v-col>
              </v-row>

              <v-text-field
                v-model="email"
                :rules="[required, emailRules]"
                label="Адрес электронной почты"
                name="email"
                color="#757575"
                prepend-inner-icon="mdi-email-outline"
                class="mt-0"
                required
              />
              <v-text-field
                v-model="password"
                :rules="[required, passwordRules]"
                label="Пароль"
                name="password"
                color="#757575"
                prepend-inner-icon="mdi-lock-outline"
                type="password"
                class="mt-0"
                required
              />

              <v-text-field
                v-model="repeatPassword"
                :rules="[required]"
                label="Повторите пароль"
                name="repeatPassword"
                color="#757575"
                prepend-inner-icon="mdi-lock-outline"
                type="password"
                class="mt-0"
                required
              />
            </v-card-text>
            <v-card-actions class="mx-0 px-0">
              <v-spacer />
              <v-btn
                :disabled="!valid"
                to="/"
                nuxt
                color="rgb(240, 55, 58)"
                class="text-capitalize white--text px-4"
                @click="validate"
              >
                Регистрация
                <v-icon
                  color="#ffffff"
                  right
                  dark
                  class="pl-2"
                >mdi-arrow-right</v-icon>
              </v-btn>
            </v-card-actions>
          </v-form>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      valid: true,
      firstname: '',
      required: v => !!v || 'Поле обязательно',
      lastname: '',
      email: '',
      emailRules: v => /.+@.+/.test(v) || 'Неверный адрес электронной почты. Введите верный адрес электронной почты',
      password: '',
      passwordRules: v => v.length >= 8 || 'Неверный пароль. Пароль должен быть не короче 8 символов',
      repeatPassword: ''
    }),
    methods: {
      validate() {
        if (this.$refs.form.validate()) {
          this.snackbar = true
        }
      }
    }
  }
</script>

<style lang="scss" scoped>
  .registration {
    max-width: 430px;

    &__title {
      font-size: 32px;
      line-height: 44px;
      color: rgb(51, 51, 51);
      padding: 40px 0 48px;
      overflow: visible;
    }
  }

</style>

<style lang="scss">
  .input-default {
    .v-label {
      font-size: 12px;
    }

    .mdi-email-outline {
      font-size: 22px;
    }
  }
</style>