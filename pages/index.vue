<template>
  <div>
    <HeroVue :title="title" :verses="verses" />

    <main>
      <v-container class="text-center">
        <section class="my-6">
          <div class="goal-div my-6 py-3">
            <h1>أكاديمية مكة المكرمة</h1>
            <p class="goal text-xl-h4 text-lg-h6 text-md-body-1 text-sm-body-2">تعلم معنا القرآن الكريم
              وتفسيره وقرآته
              المتواترة على يد
              مشايخ وعلماء متخصصين</p>
          </div>

          <h2 class='mb-5 py-3 text-decoration-underline'>القراءات</h2>
          <v-row justify="center">
            <v-col v-for="(Qeraat, i) in Qeraats" :key="i" xs="12" sm="8" md="5">
              <v-card :color="Qeraat.color" dark>
                <div class="d-flex flex-no-wrap justify-space-between">
                  <div>
                    <v-card-title class="text-h5" v-text="Qeraat.name"></v-card-title>

                    <v-card-actions>
                      <v-btn class="ml-2 mt-3" fab icon height="40px" right width="40px">
                        <v-icon>mdi-play</v-icon>
                      </v-btn>
                    </v-card-actions>
                  </div>

                  <v-avatar class="ma-3" size="125" tile>
                    <v-img :src="Qeraat.src"></v-img>
                  </v-avatar>
                </div>
              </v-card>
            </v-col>
          </v-row>
        </section>
      </v-container>
    </main>
  </div>
</template>

<script>
import HeroVue from '@/components/Hero.vue'

export default {
  name: 'IndexPage',
  components: { HeroVue },
  data() {
    return {
      title:
        '﴿ إِنَّ هَٰذَا الْقُرْآنَ يَهْدِي لِلَّتِي هِيَ أَقْوَمُ وَيُبَشِّرُ الْمُؤْمِنِينَ الَّذِينَ يَعْمَلُونَ الصَّالِحَاتِ أَنَّ لَهُمْ أَجْرًا كَبِيرًا﴾',
      verses: '[ الإسراء: 9]',
      Qeraats: [
        {
          color: '#1F7087',
          src: 'https://qurancomplex.gov.sa/wp-content/uploads/2019/09/warsh.jpg',
          name: 'ورش عن نافع',
        },
        {
          color: '#7BC6FF',
          src: 'https://qurancomplex.gov.sa/wp-content/uploads/2019/09/qalon01.jpg',
          name: 'قالون عن نافع'
        },
        {
          color: '#2E7D32',
          src: 'https://qurancomplex.gov.sa/wp-content/uploads/2019/09/hafs.jpg',
          name: 'حفص عن عاصم',
        },
        {
          color: '#00DC82',
          src: 'https://qurancomplex.gov.sa/wp-content/uploads/2019/09/shuba01.jpg',
          name: 'شعبة عن عاصم',
        },
      ]
    }
  },
}
</script>
