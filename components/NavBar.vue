<template>
  <v-card rounded="0">
    <v-toolbar app color="#A51515" class="white--text hidden-md-and-down">
      <v-spacer />
      <NuxtLink class="atalho white--text" to="/historia">História</NuxtLink>

      <v-menu
        rounded="0"
        content-class="elevation-0"
        transition="slide-y-transition"
        offset-y
        open-on-hover
      >
        <template v-slot:activator="{ on, attrs }">
          <div class="atalho" v-bind="attrs" v-on="on">
            Gestão <v-icon small color="white">mdi-menu-down</v-icon>
          </div>
        </template>
        <v-list color="#A51515">
          <v-list-item v-for="(item, index) in itemsGestao" :key="index" link>
            <v-list-item-title>
              <NuxtLink class="item white--text" :to="item.path">{{
                item.title
              }}</NuxtLink>
            </v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>

      <NuxtLink class="atalho white--text" to="/lojinha">Lojinha</NuxtLink>
      <NuxtLink class="atalho white--text" to="/">
        <v-img src="/logo.svg" position="center top" class="logo"></v-img>
      </NuxtLink>
      <v-menu
        rounded="0"
        content-class="elevation-0"
        transition="slide-y-transition"
        offset-y
        open-on-hover
      >
        <template v-slot:activator="{ on, attrs }">
          <div class="atalho" v-bind="attrs" v-on="on">
            Esportivo <v-icon small color="white">mdi-menu-down</v-icon>
          </div>
        </template>
        <v-list color="#A51515">
          <v-list-item
            v-for="(item, index) in itemsEsportivo"
            :key="index"
            link
          >
            <v-list-item-title>
              <NuxtLink class="item white--text" :to="item.path">{{
                item.title
              }}</NuxtLink>
            </v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
      <NuxtLink class="atalho white--text" to="/eventos">Eventos</NuxtLink>
      <NuxtLink class="atalho white--text" to="/contato">Contato</NuxtLink>
      <v-spacer />
    </v-toolbar>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    itemsGestao: [
      { title: "Quem Somos", path: "/quemsomos" },
      { title: "Faça Parte", path: "/participe" },
    ],
    itemsEsportivo: [
      { title: "Modalidades", path: "/modalidades" },
      { title: "Campeonatos", path: "/campeonatos" },
    ],
  }),
};
</script>

<style scoped>
.atalho {
  padding: 20px 50px;
  text-decoration: none;
}
.logo {
  margin-top: -170px;
}
.item {
  text-decoration: none;
}
</style>
