<template>
  <v-container class="teal--text darken-3">
    <v-row>
      <v-col>
        <h1>أكاديمية مكة المكرمة</h1>
        <h3>نختص بتعليم القرآن الكريم :</h3>
        <ol class="mr-5">
          <li>برواية قالون وشعبة وحفص من طريق الشاطبية</li>
          <li>تعليم التجويد النظري والعملي</li>
          <li>
            ومكتبة للتلاولات القرآنية للروايات المتواتر سندها مثل قالون وشعبة
            وحفص
          </li>
        </ol>
      </v-col>
    </v-row>

    <v-row>
      <v-col>
        <h3 class="text-right">عن المعلم :</h3>
        <p>الشيخ/ عمرو احمد فايق حسنين محمد</p>
        <p>حاصل على عدة إجازات في القرآن الكريم</p>
      </v-col>
    </v-row>

    <v-row class="certified-box">
      <v-col>
        <h3>الإجازات والشهادات :</h3>
        <ol class="mr-5">
          <li>
            إجازة في مقدمة الجزرية
          </li>
          <li>الإجازة بقراءة الامام عاصم من طريق الشاطبية</li>
          <li>إجازة في نظم تحفة الاطفال</li>
          <li>شهادة دبلوم مدكر</li>
        </ol>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'AboutPage',
  data() {
    return {
      overlay: false,
      zIndex: 1000,
    }
  },
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
