<template>
    <div>
        <h2>This is a Pop Up</h2>
        <button @click="$emit('close')">Close Pop Up</button>
    </div>
</template>

<script>
    export default {
        name: 'Pop_Up',
        emits: [close]
    }
</script>

<style scoped>

</style>