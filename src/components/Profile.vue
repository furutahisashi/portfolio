<template>
  <div class="profile">
    <h2>Profile</h2>
    <v-row>
      <v-col cols="12" xs="12" sm="12" md="6" lg="6" xl="6">
        <div class="profile-image"><a href="https://twitter.com/furutahisashi" target="_blank"></a></div>
      </v-col>
      <v-col cols="12" xs="12" sm="12" md="6" lg="6" xl="6">
        <div class="profile-text">
          <div class="line">
            <span class="left">Name</span>
            <span class="right">Hisashi Furuta</span>
          </div>
          <div class="line">
            <span class="left">Sex</span>
            <span class="right">Male♂</span>
          </div>
          <div class="line">
            <span class="left">Age</span>
            <span class="right">{{getAge()}} years old</span>
          </div>
          <div class="line">
            <span class="left">Work</span>
            <span class="right">System Engineer</span>
          </div>
          <div class="line">
            <span class="left">Favorite</span>
            <span class="right">Tennis, Bass</span>
          </div>
          <div class="line">
            <span class="left">Social</span>
            <span class="right"><a href="https://twitter.com/furutahisashi" target="_blank">Twitter</a>, <a href="https://furutahisashi.com" target="_blank">Blog</a></span>
          </div>
          <div class="line">
            <span class="left">Live</span>
            <span class="right">Nagoya</span>
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'profile',
  methods: {
    getAge: function () {
      const birth = new Date(1988, 5 - 1, 4)
      const today = new Date()
      const tyb = new Date(today.getFullYear(), birth.getMonth(), birth.getDate())
      const age = today.getFullYear() - birth.getFullYear()
      return today < tyb ? age - 1 : age
    }
  }
}
</script>

<style lang="scss" scoped>
$size: 300px;
.profile-image {
  margin: -25px auto 0;
  width: $size;
  height: $size;
  border-radius: $size / 2;
  background-position: top 0 left -50px;
  background-image: url("../assets/img/profile.jpg");
  transform: scale(0.85) scale(0.85);
  position: relative;
  a {
    position: absolute;
    left: 0;
    top: 0;
    width: $size;
    height: $size;
    border-radius: $size / 2;
  }
}
.profile-text {
  margin: 0 auto;
  @media screen and (max-width: 960px) {
    width: 310px;
  }
  font-family: ProfileFont;
  .line {
    font-size: 18pt;
    .left, .right {
      display: inline-block;
    }
    .left {
      width: 125px;
      font-weight: bold;
      color: #444;
    }
  }
  a {
    text-decoration: none;
    color: inherit;
    &:hover {
      text-decoration: underline;
    }
    &:visited {
      color: inherit;
    }
  }
}
</style>