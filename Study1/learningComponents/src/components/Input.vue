<template>
    <div>
        <input 
            type="text" 
            :value="modelValue"
            @input="$emit('update:modelValue', $event.target.value)"
        >
    </div>
</template>

<script>
    export default {
        name: 'Input_Things',
        props: {
            modelValue: String
        }
    }
</script>

<style scoped>

</style>