<template>
  <v-card width="350px" class="pa-2">
    <div class="d-flex flex-row justify-space-around">
      <v-avatar size="82">
        <v-img :src="user.picture.thumbnail" />
      </v-avatar>
    </div>
    <v-divider class="my-4"></v-divider>
    <v-card-title>
      {{ user.name.title + ' ' + user.name.first + ' ' + user.name.last }}
      <v-icon :color="user.gender === 'male' ? 'blue' : 'pink'" class="ml-2">
        {{ user.gender === 'male' ? 'mdi-gender-male' : 'mdi-gender-female' }}
      </v-icon>
    </v-card-title>
    <v-card-subtitle>
      {{ user.email }} <br />
      {{ user.cell }} <br /><br />
      {{ user.location.city }} - {{ user.location.state }} <br />
      {{ user.location.country }}
    </v-card-subtitle>
  </v-card>
</template>

<script>
export default {
  props: {
    user: {
      type: Object,
      default: () => {},
    },
  },
}
</script>
