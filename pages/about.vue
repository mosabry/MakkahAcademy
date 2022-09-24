<template>
  <v-container class="teal--text darken-3">
    <v-row>
      <v-col>
        <v-row justify="center">
          <Logo />
        </v-row>

        <!-- <h3>تعلم معنا القرآن الكريم :</h3>
        <ol class="mr-5">
          <li>برواية قالون وشعبة وحفص من طريق الشاطبية</li>
          <li>تعليم التجويد النظري والعملي</li>
          <li>
            ومكتبة للتلاولات القرآنية للروايات المتواتر سندها مثل قالون وشعبة
            وحفص
          </li>
        </ol> -->
      </v-col>
    </v-row>

    <h1>تحت التطوير</h1>
  </v-container>
</template>

<script>
import Logo from '../components/Logo.vue';
export default {
  name: "AboutPage",
  data() {
    return {
      overlay: false,
      zIndex: 1000,
    };
  },
  components: { Logo }
}
</script>

<style lang="scss">
.responsive-iframe {
  @media (min-width: 320px) {
    height: 360px;
    width: 320px;
  }

  @media (min-width: 480px) {
    height: 560px;
    width: 480px;
  }

  @media (min-width: 768px) {
    height: 780px;
    width: 560px;
  }

  @media (min-width: 1025px) {
    height: 600px;
    width: 400px;
  }

  @media (min-width: 1200px) {
    height: 480px;
    width: 640px;
  }

  @media (min-width: 1700px) {
    height: 850px;
    width: 720px;
  }
}
</style>
