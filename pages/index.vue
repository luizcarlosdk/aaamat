<template>
  <div class="main">
    <ImageCarousel :photos="photos" />
    <v-divider inset></v-divider>
    <h1>O QUE É A AAAMAT?</h1>
    <p class="content">
      A Atlética é uma instituição gerenciada pelos alunos do IME USP
      responsável pela organização de todas as modalidades esportivas,
      campeonatos dentro e fora da universidade, além da realização de festas e
      eventos de integração.
    </p>
    <h2>CONHEÇA MAIS SOBRE NÓS:</h2>

    <v-card max-width="1000" color="#3a000e">
      <div
        class="d-flex flex-no-wrap cards"
        v-for="(info, i) in cards"
        :key="info"
      >
        <v-img
          :src="require('@/assets/images/fluffy_silhueta.svg')"
          width="95px"
          height="100px"
        ></v-img>

        <div class="cardInfo">
          <v-card-title class="white--text">
            {{ cards[i].title }}
          </v-card-title>
          <v-card-text class="white--text">
            {{ cards[i].description }}
          </v-card-text>
          <v-card-actions>
            <v-btn color="red"> Ver mais </v-btn>
          </v-card-actions>
        </div>
      </div>
    </v-card>
  </div>
</template>

<script>
import ImageCarousel from "~/components/ImageCarousel.vue";
export default {
  components: {
    ImageCarousel,
  },
  data: () => ({
    photos: [
      "https://drive.google.com/uc?export=view&id=1tk-Wz6v6-arHesEk8445XM32rlcgSm78",
      "https://drive.google.com/uc?export=view&id=1m_E1lHWnMTiSRFB0sQJBnd5NrOkSs3hS",
    ],
    cards: [
      {
        title: "HISTÓRIA DA AAAMAT",
        description:
          "Toda história da fundação da atlética: ano em que foi fundada, quem foram os fundadores, primeiras arrecadações e campeonatos, ...",
      },
      {
        title: "GESTÕES DE CADA ANO",
        description:
          "Confira algumas das gestões que fizeram parte, além da atual gestão.",
      },
      {
        title: "EVENTOS",
        description:
          "Tudo sobre os eventos que a atlética organiza, como JunIME, I Will SurvIME, dentre outros; ou que participa diretamente da organização em conjunto com outras atléticas, tais como as festas do BIFE",
      },
      {
        title: "CAMPEONATOS",
        description:
          "Todos Campeonatos em que o IME participa, sendo entre as demais faculdades da USP ou não",
      },
    ],
  }),
};
</script>

<style>
.main {
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: black;
  margin: 0px 30px;
  box-shadow: 50px black;
  border-radius: 10px;
}
h1 {
  font-weight: bold;
  font-size: 30px;
  padding: 1em;
}
h2 {
  font-weight: bold;
  font-size: 25px;
  padding: 1em;
}
.content {
  padding: 0 200px;
  text-align: center;
}
.cards {
  align-items: center;
}
.cardInfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
