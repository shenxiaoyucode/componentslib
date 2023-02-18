<!-- 插槽卡片：可以指定卡片的 顶部标题、底部 以及多行的主要内容 -->
<template>
  <div class="Stars">
    <span
      v-for="starNum in 5"
      :key="starNum"
      :class="[
        'iconfont icon-star',
        starNum <=num ? 'active':''
      ]"
      :style="{fontSize: size+'px'}"
    ></span>
  </div>
</template>
<script>
  export default {
    name:"Stars",
    props: {
      num: {
        type: Number,
        default:0
      },
      size: {
        type: Number,
        default:20
      }
    },
    data(){
      return {}
    }
  }
</script>
<style scoped>
  @font-face {
  font-family: "iconfont"; /* Project id 3902604 */
  src: url('//at.alicdn.com/t/c/font_3902604_m9sw9fdqc6.woff2?t=1676647987742') format('woff2'),
       url('//at.alicdn.com/t/c/font_3902604_m9sw9fdqc6.woff?t=1676647987742') format('woff'),
       url('//at.alicdn.com/t/c/font_3902604_m9sw9fdqc6.ttf?t=1676647987742') format('truetype');
  }

  .iconfont {
    font-family: "iconfont" !important;
    font-size: 16px;
    font-style: normal;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color:darkgray
  }
  .icon-star {
    transition: color .3s;
  }
  .icon-star:before {
    content: "\e617";
  }
  .active {
    color:gold;
  } 


</style>
  