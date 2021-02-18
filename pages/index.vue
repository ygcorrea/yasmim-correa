<template>
  <v-app dark>
    <div>
      <v-app-bar
        align="baseline"
        class="col-12 hidden-md-and-down"
        color="#93b2bd"
        height="100"
        fixed
        app
      >
        <v-row
          align="center"
          justify-lg="end"
          justify-sm="center"
          style="display: flex; flex-wrap: nowrap"
          class="col-12"
          sm="6"
          md="4"
        >
          <v-btn
            v-bind="size"
            class="ma-3"
            color="white"
            @click="$vuetify.goTo('#about-me')"
          >
            <span class="black--text text--darken-1 font-weight-bold">
              Ebooks
            </span>
          </v-btn>
          <v-btn
            v-bind="size"
            class="ma-3"
            color="white"
            @click="$vuetify.goTo('#my-skills')"
          >
            <span class="black--text text--darken-1 font-weight-bold">
              Especialidades
            </span>
          </v-btn>
        </v-row>
      </v-app-bar>
      <v-main>
        <v-app>
          <section id="hero">
            <v-row no-gutters class="background-stl">
              <v-container>
                <v-theme-provider dark>
                  <v-container fill-height>
                    <v-row
                      align="center"
                      class="white--text mx-auto"
                      justify="center"
                    >
                      <v-row
                        class="white--text text-center main-text col-10"
                        style="
                          display: flex;
                          justify-content: center;
                          flex-direction: column;
                          align-items: center;
                        "
                      >
                        <span
                          :class="[
                            $vuetify.breakpoint.smAndDown
                              ? 'display-1'
                              : 'display-2',
                          ]"
                          class="font-weight-light"
                        >
                          Gabriele Gonçalves de Souza Corrêa
                        </span>
                        <br />

                        <v-row
                          justify="center"
                          align="center"
                          class="ma-3"
                          style="display: flex; flex-direction: column"
                        >
                          <v-avatar class="elevation-12 mb-0" size="220">
                            <v-img
                              src="https://user-images.githubusercontent.com/58710976/108386507-78a0f600-71eb-11eb-990c-d05d334e4ca5.png"
                            ></v-img>
                          </v-avatar>

                          <span class="ma-3 color-primary">
                            <v-icon color="#5c637c" class="ma-3"
                              >mdi-book-open-page-variant</v-icon
                            >
                            Pós Graduada em:
                          </span>
                          <small class="color-primary">
                            Nutrição clínica funcional, Psiquiatria, Sindrome de
                            Down, Nutrição com foco em autismo e TDHA
                          </small>
                          <v-row class="font-weight-bold secondary-text ma-5">
                            <small>
                              <v-icon color="#5c637c">
                                mdi-file-certificate-outline
                              </v-icon>
                              CRN 16101019
                            </small>
                          </v-row>
                        </v-row>
                      </v-row>

                      <v-row justify="center" class="ma-2">
                        <v-btn
                          color="#93b2bd"
                          target="_blank"
                          class="ma-3 width-btn"
                          href="https://api.whatsapp.com/send?phone=5521979287161"
                          large
                        >
                          <v-icon color="#5c637c">mdi-calendar-outline</v-icon>
                          <span class="ml-2 text--darken-1 font-weight-bold">
                            Agende uma consulta
                          </span>
                        </v-btn>
                        <v-btn
                          class="ma-3 width-btn"
                          target="_blank"
                          color="white"
                          href="https://api.whatsapp.com/send?phone=5521979287161"
                          large
                        >
                          <v-icon color="#93b2bd">mdi-pencil</v-icon>

                          <span
                            class="ml-2 grey--text text--darken-1 font-weight-bold"
                          >
                            Entre em contato
                          </span>
                        </v-btn>
                      </v-row>
                    </v-row>
                    <v-row>
                      <v-row justify="center" class="col-12 lista-container">
                        <span class="font-weight-bold">
                          Atendimento nutricional com foco em:
                        </span>
                      </v-row>
                      <v-row class="ma-5" justify="center">
                        <ul class="list-style">
                          <li>Autismo</li>
                          <li>TDAH</li>
                          <li>Sindrome de Down</li>
                          <li>Epilepsia</li>
                          <li>Doenças genéticas raras</li>
                        </ul>
                      </v-row>
                    </v-row>
                    <v-row justify="center" class="col-12 ma-5">
                      <v-btn
                        color="#000"
                        v-bind="size"
                        class="align-self-end"
                        fab
                        x-large
                        outlined
                        @click="$vuetify.goTo('#about-me')"
                      >
                        <v-icon>mdi-chevron-double-down</v-icon>
                      </v-btn>
                    </v-row>
                  </v-container>
                </v-theme-provider>
              </v-container>
            </v-row>
          </section>
          <section id="about-me">
            <div class="py-12"></div>

            <v-container class="text-center">
              <h2
                style="color: #93b2bd"
                class="display-2 font-weight-bold mb-3"
              >
                EBOOKS <v-icon  x-large color="#93b2bd"> mdi-book-open-outline </v-icon>
              </h2>
              <v-responsive class="mx-auto mb-8" width="56">
                <v-divider class="mb-1"></v-divider>

                <v-divider></v-divider>
              </v-responsive>

              <v-responsive
                style="overflow-x: scroll; overflow-y: hidden"
                class="mx-auto title font-weight-light mb-8"
              >
                <div class="container-ebook">
                  <span class="ebooks-list">
                    <div class="ebooks-stl">
                      <img src="@/assets/img/ebook1.JPG" alt="" />
                    </div>
                    <v-btn
                      v-bind="size"
                      download
                      class="ma-3 text-decoration-none"
                      color="white"
                      href=""
                    >
                      <span class="black--text text--darken-1 font-weight-bold">
                        Baixar Ebook
                      </span>
                    </v-btn>
                  </span>
                  <span class="ebooks-list">
                    <div class="ebooks-stl">
                      <img src="@/assets/img/ebook2.JPG" alt="" />
                    </div>
                    <v-btn
                      v-bind="size"
                      download
                      class="ma-3 text-decoration-none"
                      color="white"
                      href=""
                    >
                      <span class="black--text text--darken-1 font-weight-bold">
                        Baixar Ebook
                      </span>
                    </v-btn>
                  </span>
                  <span class="ebooks-list">
                    <div class="ebooks-stl">
                      <img src="@/assets/img/ebook3.JPG" alt="" />
                    </div>
                    <v-btn
                      v-bind="size"
                      download
                      class="ma-3 text-decoration-none"
                      color="white"
                      href=""
                    >
                      <span class="black--text text--darken-1 font-weight-bold">
                        Baixar Ebook
                      </span>
                    </v-btn>
                  </span>
                  <span class="ebooks-list">
                    <div class="ebooks-stl">
                      <img src="@/assets/img/ebook4.JPG" alt="" />
                    </div>
                    <v-btn
                      v-bind="size"
                      download
                      class="ma-3 text-decoration-none"
                      color="white"
                      href=""
                    >
                      <span class="black--text text--darken-1 font-weight-bold">
                        Baixar Ebook
                      </span>
                    </v-btn>
                  </span>
                </div>
              </v-responsive>
            </v-container>

            <div class="py-12"></div>
          </section>
          <section class="background-stl">
            <div class="py-12"></div>

            <v-container
              style="width: 100vw"
              id="my-skills"
              class="text-center"
            >
              <h2 class="display-2 font-weight-bold mb-3">Especialidades <v-icon x-large color="#fff">mdi-carrot</v-icon></h2>

              <v-responsive class="mx-auto mb-12" width="56">
                <v-divider class="mb-1"></v-divider>

                <v-divider></v-divider>
              </v-responsive>

              <Skills />
            </v-container>

            <div class="py-12"></div>
          </section>
        </v-app>
      </v-main>

      <v-footer class="justify-center" color="#93b2bd" height="40">
        <div
          class="subtitle font-weight-light black--text text--lighten-1 text-center"
        >
          &copy; {{ new Date().getFullYear() }} — Made with 💜 by Yasmim Corrêa
        </div>
      </v-footer>
    </div>
  </v-app>
</template>

<script>
import Skills from "../components/skills.vue";
import Timeline from "../components/timeline.vue";
export default {
  components: { Timeline, Skills },
  data() {
    return {
      clipped: false,
      fixed: false,
      title: "",
    };
  },
  computed: {
    size() {
      const size = { xs: "x-small", sm: "small" }[
        this.$vuetify.breakpoint.name
      ];
      return size ? { [size]: true } : {};
    },
  },
};
</script>
<style scoped>
.svgI {
  background: #93b2bd;
  border-radius: 50%;
  width: 50px;
  cursor: pointer;
}
.secondary-text {
  font-size: 20px;
  color: #5c637c;
}
.main-text {
  display: flex;
  flex-direction: column;
}
.background-stl {
  background: rgb(147, 178, 189);
  background: linear-gradient(
    203deg,
    rgba(147, 178, 189, 1) 12%,
    rgba(255, 255, 255, 1) 100%
  );
  width: 100vw;
}
.list-style {
  color: #5c637c;
}
.width-btn {
  width: 300px;
}
.ebooks-list img {
  width: 500px;
  height: 500px;
}
.ebooks-stl {
  border: 1px dashed rgb(147, 178, 189);
}
.ebooks-list {
  display: flex;
  flex-direction: column;
  margin: 10px;
  align-items: center;
}
.container-ebook {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: center;
}

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #93b2bd;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #93b2bd;
}
#about-me {
  background: #f1f1f1;
}
.lista-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 30px;
}
.lista-container span {
  font-size: 30px;
  color: #5c637c;
}
.color-primary {
  color: #5c637c;
}
</style>