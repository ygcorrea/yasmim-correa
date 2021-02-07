<template>

  <v-timeline   align-top
    :dense="$vuetify.breakpoint.smAndDown">
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      :color="year.color"
      small
    >
      <template>
        <span
          :class="`headline font-weight-bold ${year.color}--text`"
          v-text="year.year"
        ></span>
      </template>
      <v-col>
        <v-row justify="center" align="center" class="py-4">
          <h2 :class="` font-weight-bold mb-4 ${year.color}--text`">
            {{ year.text }}
          </h2>
          <v-row justify="center" align="center" class="btn-class">
            {{ year.about }}
            <v-btn
              :color="`${year.color}`"
              outlined
              class="button-style ma-3"
              :href="year.path"
              >Visit Website</v-btn
            >
          </v-row>
        </v-row>
      </v-col>
    </v-timeline-item>
  </v-timeline>
</template>
 
<script>
export default {
  data: () => ({
    years: [
      {
        text: "Cotaflix",
        color: "amber",
        path: "https://cotaflix.com/",
        year: "2020",
        about:
          "Um sistema de cotação de planos de saúde prático, responsivo e completo que atende à todos os corretores, de maneira direta, simples e prática",
      },
      {
        text: "E3mob LEP",
        color: "pink",
        path: "https://www.e3mob.com.br/",
        year: "2019",
        about:
          "LEP (Learning Experience Platform) é um conceito transformador que foca a experiência do treinando, sem deixar de observar a dimensão da gestão.",
      },

      {
        text: "Afferolab Flow",
        color: "purple",
        path: "https://leadcast.afferolab.com.br/",
        year: "2019",
        about:
          "O Flow é ecossistema de aprendizagem da Afferolab! Uma Learning Experience Plataform criada para levar a aprendizagem das organizações a outro patamar.",
      },
      {
        text: "LeadCast",
        color: "deep-orange",
        path: "https://leadcast.afferolab.com.br/",
        year: "2018",
        about:
          "Playlists multimídia com o aprendizado necessário para uma performance bem-sucedida dos líderes da sua organização.",
      },
    ],
  }),
};
</script>
<style scoped>
.btn-class {
  display: flex;
  flex-direction: column;
}
.button-style {
  width: 200px;
}
</style>