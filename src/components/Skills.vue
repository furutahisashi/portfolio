<template>
  <div class="skills">
    <h2>Skillsets</h2>
    <v-row>
      <v-col cols="12" xs="12" sm="12" md="6" lg="6" xl="6">
        <h3>Language</h3>
        <div v-for="(lang, index) in skillsets.lang" :key="index">
          <Bar class="bar" :label="lang.label" :level="lang.level" />
        </div>
      </v-col>
      <v-col cols="12" xs="12" sm="12" md="6" lg="6" xl="6">
        <h3>Framework/Library</h3>
        <div v-for="(fw, index) in skillsets.fw" :key="index">
          <Bar class="bar" :label="fw.label" :level="fw.level" />
        </div>
      </v-col>
    </v-row>
    <div class="description">
      <p>Level 5: 指導可能なレベル</p>
      <p>Level 4: 業務で使用実績有</p>
      <p>Level 3: 多分使用可能なレベル</p>
      <p>Level 2: 調べながらなんとかするレベル</p>
      <p>Level 1: 触ったことあるレベル</p>
    </div>
  </div>
</template>

<script>
import Bar from '@/components/Bar'

export default {
  name: 'skills',
  components: {
    Bar
  },
  data: function () {
    return {
      skillsets: {
        lang: [
          {label: 'C', level: 5},
          {label: 'C++', level: 5},
          {label: 'C#', level: 3},
          {label: 'HTML', level: 2},
          {label: 'CSS', level: 2},
          {label: 'Javascript', level: 3},
          {label: 'Python', level: 2},
          {label: 'PHP', level: 1},
        ],
        fw: [
          {label: 'MFC', level: 5},
          {label: 'WPF', level: 4},
          {label: 'OpenCV', level: 3},
          {label: 'OpenGL', level: 3},
          {label: 'Vue.js', level: 2},
          {label: 'Nuxt.js', level: 1},
          {label: 'jQuery', level: 2},
          {label: 'Wordpress', level: 2},
        ]
      }
    }
  }
}
</script>

<style lang="scss" scoped>
h3 {
  font-size: 150%;
  font-family: ProfileFOnt;
  text-align: center;
}
.description {
  margin: 0 auto;
  width: 260px;
  font-size: 14px;
  font-family: ProfileFont;
  color: red;
  line-height: 1em;
}
</style>