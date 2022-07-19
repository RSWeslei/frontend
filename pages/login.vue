<template>
  <v-container class="all">
    <v-row justify="space-around">
      <v-card>
        <v-container class="login">
          <v-container class="padding">
            <v-form>
              <v-text-field
                height="50"
                solo
                :outlined="showOutline1"
                color="#8257e5"
                dense
                background-color="#121214"
                label="Email"
                type="email"
                placeholder="Email"
                prepend-inner-icon="mdi-email"
                @focusin="showOutline1 = !showOutline1"
                @focusout="showOutline1 = !showOutline1"
              />
            </v-form>
            <v-form>
              <v-text-field
                height="50"
                solo
                background-color="#121214"
                :outlined="showOutline2"
                color="#8257e5"
                dense
                label="Senha"
                placeholder="Senha"
                :type="showPassword ? 'text' : 'password'"
                prepend-inner-icon="mdi-lock"
                :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                @click:append="showPassword = !showPassword"
                @focusin="showOutline2 = !showOutline2"
                @focusout="showOutline2 = !showOutline2"
              />
            </v-form>
          </v-container>
          <v-container class="submitInfo padding">
            <v-row>
              <v-container>
                <v-col class="forgetPassword">
                  <a style="color: #8257e5; text-decoration: none" href="https://app.rocketseat.com.br/forgot">Esqueci minha senha</a>
                </v-col>
              </v-container>
              <v-container class="loginButton">
                <v-col>
                  <v-btn
                    width="352px"
                    height="50"
                    class="ma-2"
                    :loading="loading"
                    :disabled="loading"
                    color="#41356b"
                    @click="loader = 'loading'"
                  >
                    ENTRAR
                  </v-btn>
                </v-col>
              </v-container>
            </v-row>
          </v-container>
        </v-container>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'LoginPages',
  data () {
    return {
      showPassword: false,
      showOutline1: false,
      showOutline2: false
    }
  }
}
</script>
<style>
  .all {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
  }
  .login {
    padding-top: 50px;
    padding-bottom: 50px;
    width: 480px;
    height: 476px;
  }
  .padding {
    padding-right: 50px;
    padding-left: 50px;
  }
  .submitInfo {
    margin-top: -60px;
    margin-left: -10px;
  }
  .forgetPassword {
    font-size: 14px;
  }
  .loginButton {
    text-align: center;
    margin-top: -30px;
  }
</style>
