<template>
    <div class="container mx-auto p-4">
        <h1 class="text-2xl md:text-3xl  lg:text-4xl font-bold mb-4">{{ post.title }}</h1>
        <p class="text-gray-700">{{ post.content }}</p>
    </div>
</template>

<script>
export default {
    name: 'BlogDetail',
    data() {
        return {
            post: {}
        }   
    },
    mounted() {
        const id = this.$route.params.id;
        const posts = [
            { id: 1, title: '博客1', content: '博客1内容 lorem ipsum dolor sit amet, consectetur adipiscing elit.' },
            { id: 2, title: '博客2', content: '博客2内容 lorem ipsum dolor sit amet, consectetur adipiscing elit.' },
            { id: 3, title: '博客3', content: '博客3内容 lorem ipsum dolor sit amet, consectetur adipiscing elit.' }
        ]
        this.post = posts.find(post => post.id === parseInt(id));
    }
}
</script>

<style scoped>
h1 {
    color: #42b983;
}
</style>