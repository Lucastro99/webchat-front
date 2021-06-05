<template>
  <span id="SiteTemplate">
    <header>
      <NavBar :cor="'dark'" :logo="'Rede Social'" :url="'/'"/>
    </header>

    <main>
      <div class="container">
        <b-row>
          <GridColum :tamanho="3" :mt="4" >
            <MenuCard>
              <Profile :type="'home'" :name="'Lucas Castro'" :descricao="'20y 🔥'" :imagem="null"/>
            </MenuCard>
          </GridColum>
          <GridColum :tamanho="9" :mt="4">
            <slot></slot>
          </GridColum>
        </b-row>
      </div>
    </main>

  </span>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import GridColum from '@/components/GridColum.vue'
import MenuCard from '@/components/MenuCard.vue'
import Profile from '@/components/Profile.vue'

export default {
  name: 'SiteTemplate',
  components: {
    NavBar,
    GridColum,
    MenuCard,
    Profile
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');
@import "../assets/scss/main.scss";

</style>
