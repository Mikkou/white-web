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
        cols="12"
        sm="8"
        md="5"
      >
        <v-card
          class="registration elevation-0 transparent"
        >
          <v-toolbar
            color="transparent"
            dark
            flat
          >
            <v-toolbar-title class="registration__title">Создать учётную запись</v-toolbar-title>
          </v-toolbar>
          <v-card-text>
            <v-form>
              <v-text-field
                label="Login"
                name="login"
                prepend-icon="mdi-account-outline"
                type="text"
              />

              <v-text-field
                id="password"
                label="Password"
                name="password"
                prepend-icon="mdi-lock"
                type="password"
              />
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-spacer />
            <v-btn color="primary">Регистрация</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
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

<style lang="scss" scoped>
  .registration {
    &__title {
      font-size: 32px;
      line-height: 44px;
      color: rgb(51, 51, 51);
      padding: 40px 0 48px;
    }
  }

</style>