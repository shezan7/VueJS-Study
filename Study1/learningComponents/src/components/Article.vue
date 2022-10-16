<template>
    <div>
        <h2>Article Content</h2>
        <h2>{{title}}</h2>
        <h2>Likes - {{likes}}</h2>
        <h2>Published - {{isPublished ? 'yes' : 'no'}}</h2>
    </div>
</template>

<script>
    export default {
       name: 'Article_Things',
       props: {
        title: {
            type: String,
            required: true,
            // default: 'Article default title'
        },
        likes: Number,
        isPublished: Boolean
       }
    }
</script>

<style scoped>

</style>