<template>
  <div>
    <b-navbar toggleable="lg" type="info" :variant="cor">
      <b-navbar-brand :href="url">{{ logo }}</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="/home">Home</b-nav-item>
          <b-nav-item href="/fotos">Fotos</b-nav-item>
          <b-nav-item href="/sobre">Sobre</b-nav-item>
        </b-navbar-nav>

        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Pesquisar"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit">Pesquisar</b-button>
          </b-nav-form>

          <b-nav-item-dropdown right>
            <template #button-content>
              <em>Usuario</em>
            </template>
            <b-dropdown-item href="/perfil">Perfil</b-dropdown-item>
            <b-dropdown-item @click="emitLogout()">Finalizar Sessão</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  props:['logo', 'url', 'cor'],
  methods:{
    emitLogout(){
      this.$router.push('/login')
    }
  }
}
</script>
<style scoped lang="scss">

</style>
