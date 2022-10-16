<template>
    <div>
        <h2>Component C</h2>
        <Component_E />
    </div>
</template>

<script>
    import Component_E from './ComponentE.vue'
    export default {
        name: 'Component_C',
        components: {
            Component_E
        }
    }
</script>

<style scoped>

</style>