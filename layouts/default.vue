<template>
  <v-app dark>
    <Header />
    <NavBar />
    <v-main>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {};
</script>

<style scoped>
.v-application {
  background-color: #3a000e;
}
</style>
