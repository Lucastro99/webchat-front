<template>
    <b-col cols="12" :sm="tamanho" :class="'mt-'+mt">
        <slot></slot>
    </b-col>
</template>

<script>
export default {
    name:'GridMenu',
    props:['tamanho', 'mt'],
}
</script>

<style lang="scss" scoped>

</style>