<template>
    <div class="mb-5">
      <b-form-group
        label="O que está acontecendo?"
        label-for="textarea-1"
      >
        <b-form-textarea
          id="textarea-1"
          v-model="post"
          placeholder="Digite aqui..."
          rows="3"
          max-rows="6"
        ></b-form-textarea>
        <b-row>
          <GridColum :tamanho="12" :mt="2" class="d-flex justify-content-end">
            <b-button class="btn-publicar" variant="success" v-if="post.length > 1">Publicar</b-button>
          </GridColum>
        </b-row>
      </b-form-group>
    </div>
</template>

<script>
import GridColum from '@/components/GridColum.vue'

export default {
  name: "Home",
  components: {
    GridColum
  },
  data() {
    return {
      post:'',
    };
  },
    
}
</script>

<style lang="scss" scoped>

</style>