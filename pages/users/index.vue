<template>
  <div>
    <h1>Users</h1>
    <ul>
      <li v-for="user in 7">
        <h2 style="cursor: pointer" @click.prevent="detailPage(user)">User - {{ user }}</h2>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  methods: {
    detailPage(id) {
      this.$router.push("/users/" + id);
    }
  }
}
</script>

<style scoped>

</style>
