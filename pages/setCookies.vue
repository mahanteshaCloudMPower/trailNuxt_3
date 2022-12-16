<template>
    <div>
      <h1> Counter: {{ counter || '-' }}</h1>
      <button @click="counter = null">
        reset
      </button>
      <button @click="counter--">
        -
      </button>
      <button @click="counter++">
        +
      </button>
    </div>
  </template>
  
  <script setup>
  const counter = useCookie('counter')
  counter.value = counter.value || Math.round(Math.random() * 1000)


  // Access to the cached value of useFetch in archive.vue
// const { data: posts } = useNuxtData('posts')
// Access to the cached value of useFetch in archive.vue
const { data: posts } = useNuxtData('posts')

console.log("set-----",data,posts)
// const { data } = await useFetch(`/api/posts/${postId}`, {
//   key: `post-${postId}`,
//   default: () => {
//     // Find the individual post from the cache and set it as the default value.
//     return posts.value.find(post => post.id === postId)
//   }
// })


  </script>
  