<template>
  <v-card width="350px" class="pa-2">
    <div class="d-flex flex-row justify-space-around">
      <v-avatar size="82">
        <v-img src="https://randomuser.me/api/portraits/thumb/women/71.jpg" />
      </v-avatar>
    </div>
    <v-divider class="my-4"></v-divider>
    <v-card-title>
      Nome completo<v-icon class="ml-2">mdi-arrow-right</v-icon>
    </v-card-title>
    <v-card-subtitle>
      email@email.com <br />
      22 933006291 <br /><br />
      Cidade - Estado <br />
      País
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
