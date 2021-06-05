<template>
  <LoginTemplate>
    <div class="grid-menu">
      <div>
        <div class="header-login">
          <p class="title animation-opacity" v-if="login">Seja Bem-Vindo!</p>
          <p class="title animation-opacity" v-else>Realizar Cadastro!</p>
          <p class="submenu animation-opacity" v-if="login">Não tem uma conta? <span @click="login = false">Cadastrar Aqui!</span></p>
          <p class="submenu animation-opacity" v-else><span @click="login = true">Voltar</span></p>
        </div>
        <div class="mt-5 inputs-login">
          <b-form-group label="Nome" label-for="textarea-1" v-if="!login" class="animation-opacity">
            <b-form-input
              v-model="name"
              placeholder="Digite seu Nome"
            ></b-form-input>
          </b-form-group>
          <b-form-group label="E-mail" label-for="textarea-1">
            <b-form-input
              v-model="email"
              placeholder="Digite seu E-mail"
            ></b-form-input>
          </b-form-group>
          <b-form-group label="Senha" label-for="textarea-1">
            <b-form-input
              v-model="password"
              type="password"
              placeholder="Digite sua Senha"
            ></b-form-input>
          </b-form-group>

          <b-row>
            <GridColum
              :tamanho="12"
              :mt="3"
            >
              <b-button class="btn-publicar animation-opacity" v-if="login">Fazer Login</b-button>
              <b-button class="btn-publicar animation-opacity" v-else>Fazer Cadastro</b-button>
              <div class="mt-3 d-flex justify-content-center animation-opacity"  v-if="login">
                <p class="reset-password">Esqueceu a senha?</p>
              </div>
            </GridColum>
          </b-row>
        </div>
      </div>
      <div class="w100">
        <img class="img-login" src="@/assets/icons/login.svg" />
      </div>
    </div>
  </LoginTemplate>
</template>

<script>
import LoginTemplate from "@/templates/LoginTemplate.vue";
import GridColum from "@/components/GridColum.vue";

export default {
  name: "Login",
  components: {
    LoginTemplate,
    GridColum,
  },
  computed: {},
  data() {
    return {
      name:"",
      email: "",
      password: "",
      login:true,
    };
  },
};
</script>

<style lang="scss" scoped>
.grid-menu {
  display: grid;
  grid-template-columns: 2fr 3fr;
  width: 100%;
  padding-top: 10vh;
}

.img-login{
  width: 100vh;
  position: absolute;
  right: 0;
}


.reset-password{
  font-family: Montserrat;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  letter-spacing: 0.1em;
  color: #8699DA;
  cursor:pointer;
}

.btn-publicar{
  height: 55px;
  background: #8699DA;
  box-shadow: 4px 8px 12px rgba(78, 99, 141, 0.06), inset 0px 4px 12px rgba(200, 211, 249, 0.6);
  border-radius: 80px;
  border:none;
  width: 100%;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  letter-spacing: 0.1em;
  color: #fff;
}

.header-login{
  .title {
    font-family: Overpass;
    font-style: normal;
    font-weight: 800;
    font-size: 36px;
    letter-spacing: 0.1em;
    color: #444b59;
  }
  
  .submenu {
    font-family: Montserrat;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 33px;
    letter-spacing: 0.1em;
    color: #444b59;
    span{
      color:#8699DA;
      font-weight: 600;
      cursor: pointer;
    }
  }
}

@media screen and (min-height: 1200px) {
  .grid-menu {
    padding-top: 25vh;
  }
  .img-login{
    width: 50vh;
  }
}
</style>
