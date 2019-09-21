<template>
  <div class="page">
    <v-container class="account-recovery">
      <v-layout column>
        <v-flex class="recovery">Восстановление аккаунта</v-flex>
        <v-flex class="envelope">
          <v-icon size="60" color="yellow darken-2">mdi-email</v-icon>
        </v-flex>
        <v-flex class="address-email">
          Адрес электронной почты аккаунта MEGA:
        </v-flex>
        <v-flex class="mail-data">
          <p>Введите адрес электронной почты учетной записи, которую вы хотите восстановить.
            Если вы не можете его вспомнить, оставьте поле пустым.</p>
        </v-flex>
        <v-flex class="address">
          <div class="email">
            <v-icon>mdi-email</v-icon>
            <input placeholder="Электронный адрес" type="email" class="email-field body-2">
          </div>
        </v-flex>
        <v-flex>
          <div>
            <v-btn class="start" depressed large color="red white--text">Старт</v-btn>
          </div>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<style lang="scss" scoped>
  .page {
    background: #f6f4f4;
    padding-top: 40px;

    .account-recovery {
      background: white;
      width: 700px;

      .address-email {
        color: grey;
        text-align: center;
        font-size: 20px;
        font-weight: bold;
      }

      .envelope {
        font-size: 40px;
        text-align: center;
        padding: 20px 0;
      }

      .recovery {
        color: #aaa;
        text-align: center;
        font-size: 20px;
      }

      .mail-data {
        text-align: center;
        padding: 20px 0;
        font-size: 15px;
      }

      .address {
        padding-left: 150px;
        padding-right: 150px;

        .email {
          padding: 5px;
          font-size: 15px;
          font-style: italic;
          border-bottom: 1px solid gray;

          .email-field {
            width: 320px;
          }
        }
      }

      .start {
        margin: 80px 270px;
        padding-left: 45px !important;
        padding-right: 45px !important;
      }
    }
  }

</style>