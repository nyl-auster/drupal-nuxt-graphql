<template>
  <section class="container">
    <h1 class="title is-1">Blog</h1>
  
    <div class="post" v-for="post in posts">
      <h3 class="title is-3">{{ post.entityLabel }}</h3>
      <hr />
    </div>
  
  </section>
</template>

<script>
import allPosts from '~/apollo/queries/allPosts'
export default {
  apollo: {
    posts: {
      query: allPosts
    }
  }
}
</script>