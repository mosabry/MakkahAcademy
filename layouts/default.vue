<template>
  <v-app class="app">
    <v-navigation-drawer class="navbar-drawer" v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app
      dark temporary>
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact>
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar class="navbar" :clipped-left="clipped" fixed app dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />

      &nbsp;
      <NuxtLink id="logo-text" to="/">
        <v-toolbar-title class="navbar-title text-xs-subtitle-1" v-text="title" />
      </NuxtLink>
      <span class="white--text slogan mobile-hidden">&nbsp; - {{slogan}}</span>
      <v-spacer />
    </v-app-bar>

    <v-main>
      <!-- <v-container> -->
      <Nuxt />
      <!-- </v-container> -->
    </v-main>

    <v-footer :absolute="!fixed" app class="footer">
      <v-spacer></v-spacer>
      <span class="year">&nbsp; {{ new Date().getFullYear() }} &copy; &nbsp;</span>
      <a href="https://mosabry.com" target="_blank">mosabry</a>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'الصفحة الرئيسية',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'عنا',
          to: '/about',
        },
        {
          icon: 'mdi-search-web ',
          title: 'تواصل معنا',
          to: '/contact',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'أكاديمية مكة المكرمة',
      slogan: 'لعلوم القرآن الكريم'
    }
  },
}
</script>

<style lang="scss">
#logo {
  width: 3rem;
}

.app {
  font-family: $main-font;
}

.navbar-drawer,
.navbar,
.footer {
  background-color: $bg-main;
}

.navbar-title {
  font-size: 1.17em;
  font-weight: bold;
}

.year {
  color: white;
}

// .v-parallax__image {
//   filter: blur(6px);
// }

.mobile-hidden{
  @media only screen and (max-width: 400px) {
    display: none;
  }
}
</style>
