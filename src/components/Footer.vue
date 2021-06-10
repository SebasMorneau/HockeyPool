<template>
  <v-footer color="primary lighten-1" padless>
    <v-row justify="center" no-gutters>
      <v-btn
        color="white"
        text
        rounded
        class="my-2"
        href="https://www.facebook.com/groups/412050072205778/"
      >
        Facebook
      </v-btn>
      <v-btn
        color="white"
        text
        rounded
        class="my-2"
        href="https://www.lepool.com/pool/52469"
      >
        Pool{{ new Date().getFullYear() }}.com
      </v-btn>
      <v-col class="primary py-4 text-center white--text" cols="12">
        {{ new Date().getFullYear() }} — <strong>Pool Joliette et cie</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    links: ["Facebook", "Pool.com"],
  }),
};
</script>