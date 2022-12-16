<!-- <template>
   <div>
    {{"mahi"}}

    <div class=""> 
       <button @click="refreshFun()">refresh</button>
       <button @click="errorFun()">  error</button>
  </div>
  
   </div>
  </template>
  <script setup>
 
 const { data, pending, error, refresh  } = await useFetch("https://jsonplaceholder.typicode.com/todos/1")
if (!data.value) {
  throw createError({ statusCode: 404, statusMessage: 'Page Not Found' })
}else{
  console.log("data----", data.value);
  // console.log("data----",JSON.stringify(JSON.parse(data.value)) )
  console.log("data----",JSON.parse(JSON.stringify(data.value))  )
}


function refreshFun(){
console.log("refresh----",refresh);
}
function errorFun(){
  console.log("error---",error)
}

  </script>
   -->


   <!-- <script setup>
   const count = ref(1)
   const { data ,error,refresh } = await useFetch(() => `https://jsonplaceholder.typicode.com/todos/${count.value}` )
   watch(count, (newCount) => {
  // Because count starts out null, you won't have access
  // to its contents immediately, but you can watch it.
  console.log("count",count?count:"","newCount",newCount)
})
   </script>
   
   <template>
     <NuxtExampleLayout example="composables/use-fetch">
       <div>
         Fetch result:
         <pre class="text-left"><code>{{ data }}</code></pre>
         <NButton @click="count++" class="rounded bg-gray-500 hover:bg-gray-900 hover:text-white py-2 px-3">
          increment
         </NButton>

         <div>
    {{ pending ? 'Loading' : count }}
  </div>
       </div>
     </NuxtExampleLayout>
   </template> -->
   

   <template>
    <div v-if="pending">
      Loading ...
    </div>
    <div v-else>
      <div v-for="post in posts">
        <!-- do something -->
        {{posts}}
        {{post}}
      </div>
    </div>
  </template>
  
  <script setup>
  /* Navigation will occur before fetching is complete.
    Handle pending and error states directly within your component's template
  */

 const count = ref(1)
  const { pending, data: posts } = useLazyFetch(`https://jsonplaceholder.typicode.com/todos/${count}`,{ key: 'posts' })
  // const { pending, data: posts } = useLazyFetch(checUrl())
  
  // We can access same data later using 'posts' key

  watch(posts, (newPosts) => {
    // Because posts starts out null, you won't have access
    // to its contents immediately, but you can watch it.
  })
  </script>
  