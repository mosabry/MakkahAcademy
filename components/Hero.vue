<template>
  <v-container>
    <v-carousel class="hero rounded-lg" hide-delimiter-background cycle height="500">
      <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src" aspect-ratio="16/9"></v-carousel-item>
    </v-carousel>
  </v-container>
</template>

<script>
export default {
  name: 'Hero',
  props: ['title', 'verses'],
  data() {
    return {
      items: [
        {
          src: 'https://i.imgur.com/uq9ftWE.jpg',
        },
        {
          src: 'https://i.imgur.com/M38VE9v.jpg',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.hero {
  border-color: #088837 #088837 #007827 !important;
}
</style>