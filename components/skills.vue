<template>
  <section id="items">
    <v-parallax
      class="col-12"
      :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
      src="https://images.unsplash.com/photo-1510915228340-29c85a43dcfe?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80"
    >
      <v-container fill-height class="col-12">
        <v-row class="mx-auto">
          <v-col v-for="(item, i) in items" :key="i">
            <div class="text-center">
              <div class="display-3 font-weight-black mb-4">
                <img
                  class="img-logo"
                  :src="require(`../assets/icons/${item.logo}`)"
                />
              </div>

              <div class="title font-weight-regular text-uppercase">
                {{ item.text }}
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-parallax>
  </section>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          logo: "js.svg",
          text: "Javascript",
        },
        {
          logo: "react.svg",
          text: "React",
        },
        {
          logo: "react.svg",
          text: "React Native",
        },
        {
          logo: "next.svg",
          text: "NextJS",
        },
        {
          logo: "vue.svg",
          text: "Vue",
        },
        {
          logo: "nuxt.svg",
          text: "NuxtJS",
        },
        {
          logo: "html.svg",
          text: "HTML5",
        },
        {
          logo: "css.svg",
          text: "CSS3",
        },
      ],
    };
  },
};
</script>

<style>
.img-logo {
  width: 70px;
}
</style>