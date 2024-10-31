<template>
    <div class="container mx-auto p-4" >
      <h1 class="text-3xl font-bold mb-4">博客列表</h1>
      <ul class="space-y-2">
        <li v-for="post in posts" :key="post.id">
           <router-link :to="{ name: 'BlogDetail', params: { id: post.id } }" class="block p-4 border rounded-lg hover:bg-gray-100">
           {{ post.title }} 
          </router-link> 
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        posts: [
          { id: 1, title: '第一篇博客' },
          { id: 2, title: '第二篇博客' },
          { id: 3, title: '第三篇博客' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  /* 自定义样式 */
  </style>
  