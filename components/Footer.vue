<template>
  <v-card rounded="0" color="#E7E6E6">
    <v-img :src="require('@/assets/images/footerTexture.svg')" height="213px">
      <div class="d-flex flex-no-wrap">
        <div class="boxLogo">
          <v-img src="/logoImeUsp.svg" max-width="113px"></v-img>
        </div>
        <v-container fluid>
          <v-row>
            <div>
              <v-card-title class="text-s1 grey--text text--darken-4">
                <strong>
                  Associação Atlética Acadêmica da Matemática (AAAMAT)
                </strong>
              </v-card-title>
              <v-card-subtitle
                class="text-subtitle-1 grey--text text--darken-4"
              >
                Instituto de Matemática e Estatística - USP
              </v-card-subtitle>
            </div>
            <div class="d-flex ml-auto">
              <v-list-item
                v-for="item in redesSociais"
                :key="item.rede"
                x-large
              >
                <a :href="item.link" target="_blank">
                  <v-icon x-large class="redesIcon">
                    mdi-{{ item.rede }}
                  </v-icon>
                </a>
              </v-list-item>
            </div>
          </v-row>
          <v-row class="d-flex justify-center">
            <hr class="footerDivider" />
          </v-row>
          <v-row>
            <v-card-text class="text-subtitle-1 grey--text text--darken-4">
              <v-icon medium color="#444">mdi-map-marker-radius</v-icon>
              Localização:
              <span class="font-weight-light">
                Rua do Matão, 1010 — Butantã, São Paulo - SP, 05508-120
              </span>
            </v-card-text>
          </v-row>
        </v-container>
      </div>
      <v-footer padless>
        <v-card dark class="text-center flex" tile flat>
          <v-card-text>
            {{ new Date().getFullYear() }} — <strong>Atlética IME USP</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </v-img>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    redesSociais: [
      {
        rede: "instagram",
        link: "https://www.instagram.com/aaamat_imeusp/",
      },
      {
        rede: "facebook",
        link: "https://pt-br.facebook.com/aaamat.ime/",
      },
      {
        rede: "linkedin",
        link: "https://br.linkedin.com/company/aaamatimeusp",
      },
    ],
  }),
};
</script>

<style scoped>
.boxLogo {
  width: 159px;
  height: 159px;
  background-color: #cecece;
  display: flex;
  align-items: center;
  justify-content: center;
}
.footerDivider {
  width: 97.5%;
  border: 0;
  height: 1px;
  background-color: #444;
}
.redesIcon {
  color: #111;
}
.redesIcon:hover {
  color: #a51515;
}
</style>
