<template>
  <div>
    <HeroVue />

    <main>
      <v-container>
        <div class="goal-div text-center my-6 py-3">
          <h1>أكاديمية مكة المكرمة لعلوم القرآن الكريم</h1>
        </div>

        <TeachersVue />
      </v-container>
    </main>
  </div>
</template>

<script>
import HeroVue from '@/components/Hero.vue'
import TeachersVue from '@/components/Teachers.vue';

export default {
  name: 'IndexPage',
  components: { HeroVue, TeachersVue }
}
</script>
