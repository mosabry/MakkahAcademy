<template>
  <!-- <v-parallax class="hero rounded-xl" dark height="600"
    src="https://images.unsplash.com/photo-1596125160970-6f02eeba00d3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1260&q=80">
    <v-row align="center" justify="center">
      <v-col class="text-center" cols="12">
        <h1 class="text-h4 mb-4 hero--title">{{ title }}</h1>
        <h4 class="subheading hero--verses">{{ verses }}</h4>
      </v-col>
    </v-row>
  </v-parallax> -->
  <v-carousel cycle height=400>
    <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src"></v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  name: 'Hero',
  props: ['title', 'verses'],
  data() {
    return {
      items: [
        {
          src: 'https://i.imgur.com/M38VE9v.jpg',
        },
        {
          src: 'https://i.imgur.com/TyDO0jv.jpg',
        },
        {
          src: 'https://i.imgur.com/Xmuw9b5.jpg',
        },
        {
          src: 'https://i.imgur.com/3i8z301.jpg',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.hero {

  // filter: blur(4px);
  &--title {
    font-family: $main-font;
  }

  &--title,
  &--verses {
    text-shadow: 0 2px 9px #000;
  }
}
</style>