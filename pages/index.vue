<template>
  <div>
    <h1>{{ name }}</h1>
    <NuxtLink to="/">Home page</NuxtLink>
    <hr>
    <NuxtLink to="/about">About page</NuxtLink>
    <hr>
    <NuxtLink to="/users">Users page</NuxtLink>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      name: "Nuxt 2 Project"
    }
  },
  // async fetch() {
  //   this.posts = await fetch('https://api.nuxtjs.dev/posts').then(res => {
  //       console.log(res.json());
  //     }
  //   );
  // }
}
</script>
