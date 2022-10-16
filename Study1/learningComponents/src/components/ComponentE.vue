<template>
    <div>
        <h2>Component E</h2>
        <Component_F />
    </div>
</template>

<script>
    import Component_F from './ComponentF.vue'
    export default {
        name: 'Component_E',
        components: {
            Component_F
        }
    }
</script>

<style scoped>

</style>