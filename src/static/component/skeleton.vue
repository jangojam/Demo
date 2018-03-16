<template>
  <div>
    <div class="skeleton" v-show="isloading">
      <div class="skeleton-head"></div>
      <div class="skeleton-body">
          <div class="skeleton-title"></div>
          <div class="skeleton-content"></div>
      </div>
    </div>
    <div v-show="!isloading">我是内容</div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        isloading: true
      }
    },
    created () {
      var _this = this
      setTimeout(function() {
        _this.isloading = false
      }, 1000);
    },
    methods: {
    }
  }
</script>


<style lang="scss" src='../css/skeleton.scss' scoped>