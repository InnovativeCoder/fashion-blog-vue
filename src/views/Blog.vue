<template>
     <div class="main">
          <h1>
               Blog Title
          </h1>
          <section class="blog-body">
               content of blog {{$route.params.id}}
               {{$data}}
          </section>
     </div>
</template>
<script>
import { defineComponent } from '@vue/composition-api';
import { useRoute, useRouter } from 'vue-router';
import data from "../data/blog-data.json";

export default defineComponent({
     setup() {
          const router = useRouter()
          const route = useRoute()
          
          return(data)
     },
})
</script>
<style>
     .blog-body{
          color:rgb(100, 100, 112)
     }
</style>
