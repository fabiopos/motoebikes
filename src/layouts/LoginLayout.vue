<template>
  <v-content>
    <v-container fluid fill-height grid-list-md text-center>
      <v-layout align-center justify-center>
        <slot />
      </v-layout>
    </v-container>
  </v-content>
</template>

<script>
export default {
  props: {
    source: String
  },
  data: () => ({
    drawer: null
  })
};
</script>