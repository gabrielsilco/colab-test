<template>
  <div class="pa-8 d-flex flex-row flex-wrap justify-space-between">
    <UserCard
      v-for="user in users"
      :key="user.login.uuid"
      :user="user"
      class="mb-6"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [],
    }
  },
  async created() {
    const result = await this.$axios.$get(
      'https://randomuser.me/api/?results=15'
    )
    this.users = result.results
  },
}
</script>
