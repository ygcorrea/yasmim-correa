<template>
  
  <section id="items" style="background: #3c415236;">
    <v-parallax
      style="width: 100vw"
      class="col-12"
      :height="$vuetify.breakpoint.smAndDown ? 500 : 400"
      src="https://user-images.githubusercontent.com/58710976/108403718-c888b880-71fd-11eb-8575-c1495d703ad3.png"
    >
      <v-container fill-height class="col-12 container-main">
        <div class="text-center">
          <v-chip x-large class="ma-2" color="rgba(147, 178, 189, 1)">
            Funcional
          </v-chip>
          <v-chip x-large class="ma-2" color="rgba(147, 178, 189, 1)">
            Alergias alimentares
          </v-chip>

          <v-chip x-large class="ma-2" color="rgba(147, 178, 189, 1)">
            Doenças autoimunes
          </v-chip>

          <v-chip x-large class="ma-2" color="rgba(147, 178, 189, 1)">
            Pediátrica
          </v-chip>
        </div>
      
      </v-container>
    </v-parallax>
  </section>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style>
.img-logo {
  width: 70px;
}
.container-main {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #3c41524f;
  justify-content: center;
}
.list-style {
  color: #3c4152;
  font-size: 20px;
}
.espec-style {
  color: #3c4152;
  font-size: 40px;
}

</style>