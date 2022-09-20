<template>
  <div>
    <h4>{{ contactText }}</h4>

    <div class="socialDiv">
      <ul>
        <li>
          <a class="icon-link" href="https://www.facebook.com/EasyTajweed.00201006026452/" target="_blank">
            <fa class="icon facebook" :icon="['fab', 'facebook']" />
            {{ socialIcons.facebook }}
          </a>
        </li>
        <li>
          <a class="icon-link" href="https://t.me/MakkahAcademyforHolyQuran" target="_blank">
            <fa class="icon telegram" :icon="['fab', 'telegram']" />
            {{ socialIcons.telegram }}
          </a>
        </li>
        <li>
          <a class="icon-link" href="#">
            <fa class="icon whatsapp" :icon="['fab', 'whatsapp']" />
            {{socialIcons.whatsapp[1]}}
          </a>
        </li> <li>
          <a class="icon-link" href="#">
            <fa class="icon whatsapp" :icon="['fab', 'whatsapp']" />
            {{socialIcons.whatsapp[2]}}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Logo from './Logo.vue';
export default {
  name: "Social",
  data() {
    return {
      contactText: "  يمكنك التواصل معنا للأستفسار عن طريق الروابط التالية :",
      socialIcons: {
        facebook: "Facebook",
        telegram: "Telegram",
        whatsapp: ["Whatsapp", "00201006026452", "00994409571238"]
      },
    };
  },
  components: { Logo }
}
</script>

<style lang="scss" scoped>
.icon-link {
  color: $main-color;

  .icon {
    font-size: 40px;
    vertical-align: middle;
    line-height: 10px;
  }

  &:hover {
    .icon {
      color: #81C784;
    }
  }
}

.facebook {
  color: rgb(59, 91, 152);
}

.twitter {
  color: #1da1f2;
}

.telegram {
  color: #0088cc;
}

.whatsapp {
  color: #25d366;
}
</style>
