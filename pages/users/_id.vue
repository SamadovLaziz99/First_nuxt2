<template>
  <div>
    <h1>Name - {{ user.name }}</h1>
    <hr>
    <h3>{{ user.email }}</h3>
    <h3>{{ user.phone }}</h3>
  </div>
</template>
<script>
export default {
  validate({params}) {
    return /^\d+$/.test(params.id);
  },
  async asyncData({$axios, params}) {
    const user = await $axios.$get("https://jsonplaceholder.typicode.com/users/" + params.id);
    return {user}
  },
}
</script>

<style scoped>

</style>
