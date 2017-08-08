<template>
  <section class="container">
    <h1 class="title is-1">Blog</h1>
  
    <div v-if="nodeQuery" class="post" v-for="post in nodeQuery.entities">
      <h3 class="title is-3">{{ post.entityLabel }}</h3>
      <div class="body">{{ post.body }} </div>
      <hr />
    </div>
  
  </section>
</template>

<script>
import allPosts from '~/apollo/queries/allPosts'
export default {
  apollo: {
    nodeQuery: {
      prefetch: true,
      query: allPosts
    }
  }
}
</script>