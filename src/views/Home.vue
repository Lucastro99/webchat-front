<template>
  <SiteTemplate>
    <PublishContent></PublishContent>
    <div>
      <ContentPost
        :titulo="''"
        :imagem="img"
        :descricao="desc"
        :perfil="null"
        :name="'Lucas Castro'"
        :data="'15/05/2021 - 02:45'"
      ></ContentPost>
    </div>
  </SiteTemplate>
</template>

<script>
import ContentPost from "@/components/ContentPost.vue";
import PublishContent from '@/components/PublishContent.vue'
import SiteTemplate from '@/templates/SiteTemplate.vue'

export default {
  name: "Home",
  components: {
    SiteTemplate,
    ContentPost,
    PublishContent,
  },
  computed: {
  },
  data() {
    return {
      post:'',
      img: "https://picsum.photos/300/150/?image=41",
      desc:
        "Some quick example text to build on the card title and make up the bulk of the card's content.",
    };
  },
};
</script>

<style lang="scss" scoped>
.btn-publicar:hover{
  transform: scale(1.1);
}
</style>
