<template>
  <div class="works">
    <h2>Works</h2>
    <v-row>
      <v-col cols="12" xs="12" sm="12" md="6" lg="4" xl="4" v-for="(data, index) in datas" :key="index">
        <v-card class="card">
          <v-card-title>{{data.title}}</v-card-title>
          <v-card-text>{{data.description}}</v-card-text>
          <a class="link" :href="data.url" target="_blank"></a>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'works',
  data: function () {
    return {
      datas: [
        {title: 'Lottery', url: 'https://appli.cc/lottery', description: 'プレゼント企画などで使える抽選機です。'},
        {title: 'TextCounter', url: 'https://appli.cc/textcounter', description: 'テキストのあれこれをカウントするツールです。'},
        {title: 'TextIndexing', url: 'https://appli.cc/textindexing', description: 'テキスト中の指定文字をインデックスするツールです。'},
        {title: 'TextPinch', url: 'https://appli.cc/textpinch', description: 'テキストを指定テキストで挟むツールです。'},
        {title: 'TextRepeat', url: 'https://appli.cc/textrepeat', description: 'テキストを繰り返すツールです。'},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.card {
  font-family: "Nico Moji";
  position: relative;
  .link {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
  }
}
</style>