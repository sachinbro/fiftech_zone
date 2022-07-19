<template>
 <v-app>
  <Header />
  <v-main>

      <Nuxt />
  </v-main>
 </v-app>
</template>

<script>
import Header from '../components/Header.vue'
export default {
    name: "DefaultLayout",
    data() {
        return {};
    },
    components: { Header }
}
</script>
