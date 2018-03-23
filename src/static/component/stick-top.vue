<template>
  <div>
    <div ref="A" class="A">
      <p>东风浩荡东风浩荡东风浩荡</p> 
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p> 
    </div>
    <div class="B"  :class="stick ? 'topFix': ''"></div>
    <div class="B" v-show="stick"></div>
    <div class="C">
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>  
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>   
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p> 
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p>
      <p>东风浩荡东风浩荡东风浩荡</p> 
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        stick: false,
        
      }
    },
    mounted() {
      
    },
    created() {
      this.$nextTick(function(){
        window.addEventListener('scroll',this.scrollFb)
      })
    },
    computed: {
    },
    methods: {
      scrollFb: function() {
        var scrollTop = document.documentElement.scrollTop || document.body.scrollTop
        var AHeight = this.$refs.A.offsetHeight
        console.log(scrollTop,AHeight)
        if(scrollTop >= AHeight){
          this.stick = true;
        } else {
          this.stick = false;
        }
      }
    }

  }
</script>


 <style lang="scss" src="../css/stick-top.scss" scoped>
 </style>