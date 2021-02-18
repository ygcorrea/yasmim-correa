<template>
  <v-app dark>
    <div>
      <v-app-bar
        align="baseline"
        class="col-12"
        color="black"
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
          <a
            class="hidden-sm-and-down ma-3"
            v-bind="size"
            href="https://github.com/ygcorrea"
          >
            <img class="svgI" src="@/assets/icons/github.png" alt="github" />
          </a>
          <v-btn
            v-bind="size"
            class="ma-3"
            color="white"
            outlined
            @click="$vuetify.goTo('#my-skills')"
          >
            <span class="white--text text--darken-1 font-weight-bold sparkle u-hover--sparkle">
              Skills
            </span>
          </v-btn>
          <v-btn
            v-bind="size"
            outlined
            class="ma-3"
            color="white"
            @click="$vuetify.goTo('#my-projects')"
          >
            <span class="white--text text--darken-1 font-weight-bold sparkle u-hover--sparkle">
              Projects
            </span>
          </v-btn>
          <v-btn
            v-bind="size"
            outlined
            download
            class="ma-3 pa-0 text-decoration-none"
            color="white"
            href="https://drive.google.com/u/0/uc?id=1ZJ9l22xcqSDZvDzLK42fuIBKDn4fhBDG&export=download"
          >
            <span
              class="white--text text--darken-1 font-weight-bold sparkle u-hover--sparkle"
            >
              Download CV
            </span>
          </v-btn>
        </v-row>
      </v-app-bar>
      <v-divider />
      <v-main>
        <v-app>
          <section id="hero">
            <v-row no-gutters>
              <v-img
                :max-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
                src="https://user-images.githubusercontent.com/58710976/107124919-4d321900-6885-11eb-8d10-237312816eb3.png"
              >
                <v-theme-provider dark>
                  <v-container fill-height>
                    <v-row
                      align="center"
                      class="white--text mx-auto"
                      justify="center"
                    >
                      <v-col class="white--text text-center" cols="12" tag="h1">
                        <span
                          :class="[
                            $vuetify.breakpoint.smAndDown
                              ? 'display-1'
                              : 'display-2',
                          ]"
                          class="font-weight-light"
                        >
                          WELCOME TO
                        </span>

                        <br />

                        <span
                          :class="[
                            $vuetify.breakpoint.smAndDown
                              ? 'display-3'
                              : 'display-4',
                          ]"
                          class="font-weight-black"
                        >
                          MY PORTFOLIO
                        </span>
                      </v-col>

                      <v-btn
                        v-bind="size"
                        class="align-self-end"
                        fab
                        large
                        outlined
                        @click="$vuetify.goTo('#about-me')"
                      >
                        <v-icon>mdi-chevron-double-down</v-icon>
                      </v-btn>
                    </v-row>
                  </v-container>
                </v-theme-provider>
              </v-img>
            </v-row>
          </section>
          <section id="about-me">
            <div class="py-12"></div>

            <v-container class="text-center">
              <v-responsive class="mx-auto mb-8" width="56">
                <v-divider class="mb-1"></v-divider>

                <v-divider></v-divider>
              </v-responsive>

              <v-responsive
                class="mx-auto title font-weight-light mb-8"
                max-width="720"
              >
                <h3>HELLO WORLD</h3>
                <h2 class="display-2 font-weight-bold mb-3">
                  I'M YASMIM CORRÊA
                </h2>

                <span
                  >i'm a Software developer and a passionate about Javascript,
                  science, physics and technology 🤘.</span
                >
                <p>
                  I have about 3 years of experience with web and mobile
                  development
                </p>
              </v-responsive>

              <v-avatar class="elevation-12 mb-12" size="128">
                <v-img
                  src="https://user-images.githubusercontent.com/58710976/107131372-6f8f5b00-68b4-11eb-8557-de2f8c2b73c2.JPG"
                ></v-img>
              </v-avatar>

              <div></div>
              <v-btn
                class="ma-2"
                color="white"
                href="https://github.com/ygcorrea"
                large
              >
                <img src="@/assets/icons/github.png" alt="github" />
                <span class="grey--text text--darken-1 font-weight-bold">
                  Github
                </span>
              </v-btn>
              <v-btn
                class="ma-3"
                color="white"
                href="https://www.linkedin.com/in/ygcorrea/"
                large
              >
                <img src="@/assets/icons/linkedin.png" alt="linkedin" />

                <span class="ml-2 grey--text text--darken-1 font-weight-bold">
                  Linkedin
                </span>
              </v-btn>
            </v-container>

            <div class="py-12"></div>
          </section>
          <section class="black">
            <div class="py-12"></div>

            <v-container
              style="width: 100vw"
              id="my-skills"
              class="text-center black"
            >
              <h2 class="display-2 font-weight-bold mb-3">SKILLS</h2>

              <v-responsive class="mx-auto mb-12" width="56">
                <v-divider class="mb-1"></v-divider>

                <v-divider></v-divider>
              </v-responsive>

              <Skills />
            </v-container>

            <div class="py-12"></div>
          </section>
          <section id="features">
            <div class="py-12"></div>
            <v-divider />
            <v-container id="my-projects" class="text-center">
              <h2 class="display-2 font-weight-bold mb-3">
                PROJECTS THAT I WORKED ON
              </h2>

              <v-responsive class="mx-auto mb-12" width="56">
                <v-divider class="mb-1"></v-divider>

                <v-divider></v-divider>
              </v-responsive>

              <Timeline />
            </v-container>

            <div class="py-12"></div>
          </section>
          <v-divider />
        </v-app>
      </v-main>

      <v-footer class="justify-center" color="#292929" height="40">
        <div
          class="subtitle font-weight-light grey--text text--lighten-1 text-center"
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
  background: whitesmoke;
  border-radius: 50%;
  width: 50px;
  cursor: pointer;
}
</style>
<style lang="scss" scoped>
.sparkle {
  max-width: 10em;
  color: $c-text;
  margin: auto auto;
  &:hover {
    cursor: pointer;
  }
}

.u-hover--sparkle {
  box-sizing: border-box;
  position: relative;
  padding: 0.75em;
  &::before,
  &::after {
    content: "";
    box-sizing: border-box;
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    transform-origin: center;
  }

  &::before {
    border-top: 0.2em solid $c-border;
    border-bottom: 0.2em solid $c-border;
    transform: scale3d(0, 1, 1);
  }

  &::after {
    border-left: 0.2em solid $c-border;
    border-right: 0.2em solid $c-border;
    transform: scale3d(1, 0, 1);
  }

  &:hover::before,
  &:hover::after {
    transform: scale3d(1, 1, 1);
    transition: transform 900ms;
  }
}
</style>
