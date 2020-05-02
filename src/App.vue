<template>
  <v-app>
    <v-app-bar app color="gray accent-4" dark>
      <v-toolbar-title>
        <span class="header-title">Hisashi Furuta's Portfolio</span>
      </v-toolbar-title>
    </v-app-bar>
    <v-content>
      <v-container fluid>
        <Profile />
        <Skills />
        <Works />
      </v-container>
    </v-content>
    <v-footer dark>
      <div class="flex-grow-1"></div>
      <span class="copy">&copy; {{(new Date()).getFullYear()}} <a href="https://furutahisashi.com" target="_blank">フルタヒサシ</a>.</span>
    </v-footer>
  </v-app>
</template>

<script>
import Profile from '@/components/Profile'
import Skills from '@/components/Skills'
import Works from '@/components/Works'

export default {
  name: 'App',
  components: {
    Profile,
    Skills,
    Works
  }
};
</script>

<style lang="scss">
@font-face {
  font-family: 'ProfileFont';
  src: url("./assets/font/851tegaki_zatsu_normal_0883.ttf");
}
h2 {
  font-size: 200%;
  font-family: ProfileFont;
  text-align: center;
}
.header-title {
  font-size: 120%;
  font-family: ProfileFont;
}
.copy {
  a {
    color: inherit;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
    &:visited {
      color: inherit;
    }
  }
}
</style>
