<template>
  <span id="LoginTemplate">
    <main>
      <div class="container">
        <b-row class="d-flex justify-content-center align-bottom">
          <GridColum :tamanho="12" :mt="''" class="">
            <slot></slot>
          </GridColum>
        </b-row>
      </div>
    </main>

  </span>
</template>

<script>
import GridColum from '@/components/GridColum.vue'

export default {
  name: 'LoginTemplate',
  components: {
    GridColum,
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');
@import "../assets/scss/main.scss";

</style>
