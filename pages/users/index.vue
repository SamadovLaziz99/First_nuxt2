<template>
  <div>
    <h1>
      <NuxtLink to="/">Back to home</NuxtLink>
    </h1>
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="user in users">
        <h2 style="cursor: pointer" @click.prevent="detailPage(user.id)">{{ user.name }}</h2>
        <hr>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: "This is Users List"
  }),
  async asyncData({$axios}) {
    const users = await $axios.$get("https://jsonplaceholder.typicode.com/users");
    return {users}
  },
  methods: {
    detailPage(id) {
      this.$router.push("/users/" + id);
    }
  }
}
</script>

<style scoped>

</style>
