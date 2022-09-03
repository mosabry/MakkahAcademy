<template>
  <v-container class="teal--text darken-3">
    <v-row>
      <v-col>
        <h1>نور مبين</h1>
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
            <v-btn class="white--text" color="teal" @click="overlay = !overlay">
              عرض
              <v-icon dark right>
                mdi-checkbox-marked-circle
              </v-icon>
            </v-btn>

            <v-overlay :z-index="zIndex" :value="overlay">
              <v-col>
                <v-row>
                  <div class="pdf-container">
                    <iframe src="https://drive.google.com/file/d/1qVddrVTvUf0TIrDnfvu0YgOWrHg6zwuY/preview"
                      class="responsive-iframe" allow="autoplay"></iframe>
                  </div>
                </v-row>
                <v-row justify="center">
                  <v-btn class="white--text my-5" color="red" @click="overlay = false">
                    غلق
                    <v-icon dark right>
                      mdi-close-marked-circle
                    </v-icon>
                  </v-btn>
                </v-row>
              </v-col>
            </v-overlay>
          </li>
          <li>الإجازة بقراءة الامام عاصم من طريق الشاطبية
            <v-btn class="white--text" color="teal" @click="overlay = !overlay">
              عرض
              <v-icon dark right>
                mdi-checkbox-marked-circle
              </v-icon>
            </v-btn>

            <v-overlay :z-index="zIndex" :value="overlay">
              <v-col>
                <v-row>
                  <div class="pdf-container">
                    <iframe src="https://drive.google.com/file/d/1qVddrVTvUf0TIrDnfvu0YgOWrHg6zwuY/preview"
                      class="responsive-iframe" allow="autoplay"></iframe>
                  </div>
                </v-row>
                <v-row justify="center">
                  <v-btn class="white--text my-5" color="red" @click="overlay = false">
                    غلق
                    <v-icon dark right>
                      mdi-close-circle
                    </v-icon>
                  </v-btn>
                </v-row>
              </v-col>
            </v-overlay>
          </li>
          <li>إجازة في نظم تحفة الاطفال
            <v-btn class="white--text" color="teal" @click="overlay = !overlay">
              عرض
              <v-icon dark right>
                mdi-checkbox-marked-circle
              </v-icon>
            </v-btn>

            <v-overlay :z-index="zIndex" :value="overlay">
              <v-col>
                <v-row>
                  <div class="pdf-container">
                    <iframe src="https://drive.google.com/file/d/1qVddrVTvUf0TIrDnfvu0YgOWrHg6zwuY/preview"
                      class="responsive-iframe" allow="autoplay"></iframe>
                  </div>
                </v-row>
                <v-row justify="center">
                  <v-btn class="white--text my-5" color="red" @click="overlay = false">
                    غلق
                    <v-icon dark right>
                      mdi-close-circle
                    </v-icon>
                  </v-btn>
                </v-row>
              </v-col>
            </v-overlay>
          </li>
          <li>شهادة دبلوم مدكر
            <v-btn class="white--text" color="teal" @click="overlay = !overlay">
              عرض
              <v-icon dark right>
                mdi-checkbox-marked-circle
              </v-icon>
            </v-btn>

            <v-overlay :z-index="zIndex" :value="overlay">
              <v-col>
                <v-row>
                  <div class="pdf-container">
                    <iframe src="https://drive.google.com/file/d/1qVddrVTvUf0TIrDnfvu0YgOWrHg6zwuY/preview"
                      class="responsive-iframe" allow="autoplay"></iframe>
                  </div>
                </v-row>
                <v-row justify="center">
                  <v-btn class="white--text my-5" color="red" @click="overlay = false">
                    غلق
                    <v-icon dark right>
                      mdi-close-circle
                    </v-icon>
                  </v-btn>
                </v-row>
              </v-col>
            </v-overlay>
          </li>
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
