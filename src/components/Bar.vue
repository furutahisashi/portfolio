<template>
  <div class="bar">
    <span class="label">{{label}}</span>
    <span class="level">
      <span class="level-bar" :style="{width: bar_width + 'px'}"></span>
      <span class="level-label">Level {{level}}</span>
    </span>
  </div>
</template>

<script>
export default {
  name: 'bar',
  props: ['label', 'level'],
  data: function () {
    return {
      bar_width: 0
    }
  },
  mounted: function () {
    this.bar_width = this.level * 40 - 2
  }
}
</script>

<style lang="scss" scoped>
.bar {
  margin: 3px auto;
  width: 320px;
  font-size: 20px;
  .label {
    display: inline-block;
    width: 120px;
  }
  .level {
    border: solid 1px #aaa;
    display: inline-block;
    width: 200px;
    height: 30px;
    position: relative;
    .level-bar {
      display: inline-block;
      height: 28px;
      background-color: #afa;
    }
    .level-label {
      padding-left: 5px;
      display: inline-block;
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
    }
  }
}
</style>