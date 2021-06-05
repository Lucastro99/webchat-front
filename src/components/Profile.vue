<template>
    <div>
        <b-media tag="li">
            <template #aside>
            <b-img rounded="circle" blank blank-color="#333" :src="imagem" width="55" alt="placeholder"></b-img>
            </template>
            <h5 class="mt-0 mb-1">{{name}}</h5>
            <p class="mb-0">{{descricao}}</p>
        </b-media>
    </div>
</template>

<script>
export default {
    props:['type', 'name', 'descricao', 'imagem']
}
</script>

<style lang="scss" scoped>

</style>