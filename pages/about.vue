<template>
  <v-container>
    <v-row>
      <v-col>
        <v-row justify="center">
          <Logo />
        </v-row>
        <h1>أكاديمية مكة المكرمة</h1>

        <main>
          <h2>هيا بنا نتعلم كتاب الله على
            أيدي معلمين معتمدين من الأزهر الشريف
            ومؤهلين من الجمعية الخيرية لتحفيظ القرآن الكريم بالسعودية</h2>

          <v-list>
            <v-list-item class="text-md-h6">
              نختص بعلوم القرآن الكريم والسنة النبوية
            </v-list-item>
            <v-list-item class="text-md-h6">شرح متون وقواعد التجويد</v-list-item>
            <v-list-item class="text-md-h6">شرح متني الشاطبي والدرة</v-list-item>
          </v-list>


        </main>
      </v-col>
    </v-row>
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
