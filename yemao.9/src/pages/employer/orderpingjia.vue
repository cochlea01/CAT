<template>
  <div class="">
    <div class="header">
      <div class="header-left" @click="goback"><img src="../../../static/images/index/back.png"/></div>
      <span>订单评价</span>
      <div class="header-right">完成</div>
    </div>
    <!--评价内容-->
    <div class="pj-content">
      <div class="pc-top">
        <div class="pt-tu"><img src="../../../static/images/bj.jpg"></div>
        <div class="pt-nichen"><span>昵称</span></div>
      </div>
      <!--星星评分-->
      <div class="pc-xing">
        <ul>
          <li>
            <div class="px-left">图纸满意度</div>
            <div class="px-right">
                <rater v-model="data5"  active-color="#FF9900" :margin="0"></rater>
            </div>
          </li>
          <li>
            <div class="px-left">图纸满意度</div>
            <div class="px-right">
              <rater v-model="data5"  active-color="#FF9900" :margin="0"></rater>
            </div>
          </li>
          <li>
            <div class="px-left">图纸满意度</div>
            <div class="px-right">
              <rater v-model="data5"  active-color="#FF9900" :margin="0"></rater>
            </div>
          </li>
        </ul>
      </div>
      <!--留言-->
    <div class="pc-shuru">
        <textarea class="area" maxlength="200" placeholder="对作品还满意吗？"></textarea>
        <p class="xianzhi"><span class="zs">100</span>/<span>100</span></p>
    </div>
    </div>
  </div>
</template>

<script>
  import { Rater,Cell} from 'vux'
  export default {
    components: {
      Rater,
      Cell,
    },
    data () {
      return {
          data5:4,
      }
    },
    methods: {
      goback(){
        this.$router.goBack();
      },
      toUrl: function (pagename) {
        this.$router.push({name: pagename})
      },
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import "../../assets/css/public/public.css";
  @import "../../assets/css/employer/order-pingjia.css";
</style>
