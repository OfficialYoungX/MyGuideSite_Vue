<template>
    <a v-bind:href="href">{{ text }}</a>
</template>

<script>
export default {
    name: 'TargetLink',
    props: {
        text: String,
        href: String
    }
}
</script>

<style lang="scss" scoped>
    a{
        font-size: 3.4rem;
        text-decoration:none; 
        &:active{
            text-decoration: none;
            text-decoration-line: none;
        }
        &:visited{
            text-decoration: none;
            text-decoration-line: none;
        }
    }

    
</style>