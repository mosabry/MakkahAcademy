<template>
  <div>
    <HeroVue :title="title" :verses="verses" />
  </div>
</template>

<script>
import HeroVue from '../components/Hero.vue'

export default {
  name: 'IndexPage',
  components: { HeroVue },
  data() {
    return {
      title:
        '﴿ إِنَّ هَٰذَا الْقُرْآنَ يَهْدِي لِلَّتِي هِيَ أَقْوَمُ وَيُبَشِّرُ الْمُؤْمِنِينَ الَّذِينَ يَعْمَلُونَ الصَّالِحَاتِ أَنَّ لَهُمْ أَجْرًا كَبِيرًا﴾',
      verses: '[ الإسراء: 9]',
    }
  },
}
</script>
