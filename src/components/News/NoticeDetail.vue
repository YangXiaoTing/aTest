<template>
  <div class="NoticeDetail">
    <div class="NoticeDetailTitle" v-text="article.Title"></div>
    <div class="NoticeCurPage">
      当前位置：公告> <span v-text="article.Title"></span>
      <span class="SetupTime" v-text="article.SetupTime"></span>
    </div>
    <div class="NoticeContent" v-html="article.Content">
    </div>
    <div class="NoticeBtnItem">
      <router-link to="/News/Notice" tag="button">
        返回公告列表
      </router-link>
      <!--<button>下一篇</button>-->
    </div>
  </div>
</template>

<script>
  export default {
    name: 'NoticeDetail',
    data () {
      return {
        noticeID: '',
        article: {
          Title: '关于“威特金融帝国”手续费通知',
          Content: `尊敬的各位玩家，VTS股票平台已经全部开放，“威特金融帝国交易系统”将于2017年9月18日15时开启VT提现功能，届时VT转换SC将扣除10%的ⅤT作为平台推广费用，望各位玩家相互转告。`,
          SetupTime: '2017-09-18 08:00'
        }
      }
    },
    beforeRouteEnter: (to, from, next) => {
      next(vm => {
        vm.noticeID = vm.$route.params.NoticeI
      })
    },
    methods: {
    }
  }
</script>

<style scoped>
  .NoticeDetail{
    color: #fff;
    width: 80%;
    height: 800px;
    margin: 86px auto;
    max-width: 988px;
  }
  .NoticeDetailTitle{
    text-align: center;
    font-size: 16px;
    border-bottom: 1px solid rgba(255,255,255,.3);
    padding: 0 0 24px 0;
  }
  .NoticeCurPage{
    margin: 10px 0 40px 0 ;
    position: relative;
  }
  .NoticeCurPage .SetupTime{
    position: absolute;
    right: 0;
  }
  .NoticeContent{
    margin: 0 84px;
    line-height: 30px;
  }
  .NoticeBtnItem{
    margin: 100px 84px 0 0;
    text-align: right;
  }
  .NoticeBtnItem button{
    display: inline-block;
    border: none;
    padding: 10px 20px;
    height: 36px;
    border-radius: 3px;
    background-color: rgba(255,255,255,.1);
    text-align: center;
    color: #fff;
    cursor: pointer;
  }

</style>
