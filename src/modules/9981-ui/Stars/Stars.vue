<!-- 星星评分组件 -->
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
<style>
  @font-face {
  font-family: "iconfont"; /* Project id 3902604 */
  src: url('//at.alicdn.com/t/c/font_3902604_whrc6lwghsn.woff2?t=1676736211404') format('woff2'),
       url('//at.alicdn.com/t/c/font_3902604_whrc6lwghsn.woff?t=1676736211404') format('woff'),
       url('//at.alicdn.com/t/c/font_3902604_whrc6lwghsn.ttf?t=1676736211404') format('truetype');
  }

  .iconfont {
    font-family: "iconfont" !important;
    font-size: 16px;
    font-style: normal;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color:darkgray
  }
  .icon-star:before {
    content: "\e617";
  }
  .icon-star {
    transition: color .3s;
  }
  .active {
    color:gold;
  } 

</style>
