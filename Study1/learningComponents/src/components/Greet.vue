<template>
    <div>
        <h2>Helloooo {{name}} from {{channelName}} </h2>
    </div>
</template>

<script>
    export default {
        name: 'Greet_Things',
        props: ['name', 'channelName']
    }
</script>

<style scoped>

</style>