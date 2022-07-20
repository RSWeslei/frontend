<template>
  <v-container class="all">
    <v-row justify="center">
      <v-card>
        <v-container class="login">
          <v-col>
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
          </v-col>
          <v-col align="center">
            <v-container class="submitInfo">
              <v-row>
                <v-container>
                  <v-col class="forgetPassword">
                    <a style="color: #8257e5; text-decoration: none" href="https://app.rocketseat.com.br/forgot">Esqueci minha senha</a>
                  </v-col>
                </v-container>
                <v-container>
                  <v-col class="loginButton">
                    <v-btn
                      width="352px"
                      height="50"
                      color="#41356b"
                      depressed="true"
                      disabled
                    >
                      ENTRAR
                    </v-btn>
                  </v-col>
                </v-container>
                <v-container>
                  <v-col>
                    <b style="padding-right: 6px" >Nao tem uma conta?</b>
                    <a
                      class="link"
                      href="https://app.rocketseat.com.br/signup"
                    >
                      Registre-se
                    </a>
                  </v-col>
                </v-container>
              </v-row>
            </v-container>
          </v-col>
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
      showOutline2: false,
      mouseOver: false
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
    /* background-color: brown; */
  }
  .padding {
    padding-right: 40px;
    padding-left: 40px;
    /* background-color: chartreuse; */
  }
  .submitInfo {
    margin-top: -60px;
    /* background-color: blue; */
  }
  .forgetPassword {
    font-size: 14px;
    padding-right: 220px;
    margin-top: -20px;
  }
  .loginButton {
    margin-top: -30px;
    width: fit-content;
    /* background-color: #FF0000; */
  }
  .loginButton:hover {
    cursor: not-allowed;
  }
  .link {
    text-decoration: none;
    color: #FF0000;
  }
  .link:hover {
    color:rgb(130, 87, 229);
  }
</style>
