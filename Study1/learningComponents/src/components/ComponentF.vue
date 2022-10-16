<template>
    <div>
        <h2>Component F</h2>
        <h3>Component F username {{username}}</h3>
    </div>
</template>

<script>
    export default {
        name: 'Component_F',
        inject: ['username']
    }
</script>

<style scoped>

</style>