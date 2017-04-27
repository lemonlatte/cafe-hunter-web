<style lang="sass" scoped>
$color_coffee: #895737
$color_darkcoffee: #5e3023
$color_back: #f7f7f2
$color_secondary: #9bc1a2

*
  // border: solid 1px black
  position: relative
  vertical-align: middle
  margin: 0
  padding: 0
  box-sizing: border-box
  font-size: 16px
  font-family: 'Open Sans', sans-serif
  color: $color_darkcoffee

html,body
  width: 100%
  height: 100%
  background-color: #222

.screen
  width: 375px
  height: 667px
  position: absolute
  background-image: url("http://i.imgur.com/RUJe0IH.png")
  background-size: cover
  left: 50%
  top: 50%
  transform: translateX(-50%) translateY(-50%)

.page
  width: 100%
  height: 60%
  background-color: $color_back
  position: absolute
  bottom: 0px
  border-radius: 10px 10px 0 0
  box-shadow: 0 0 10px rgba(0,0,0,0.5)
  overflow: hidden

.header
  // height: 30px
  padding: 10px 15px 10px 15px
  color: white
  background-color: $color_coffee

.container
  height: 280px
  margin: 0 15px
  overflow: auto

.description,.remark
  margin: 15px 0

.remark
  font-size: 14px
  color: $color_secondary

.row
  margin: 15px 0px
.inputbox
  width: 50%
  position: absolute
  right: 0
.inputbox,.text,.minus,.num,.plus
  display: inline-block
  color: $color_darkcoffee
.minus,.num,.plus
  width: calc(100% / 3 - 5px)
  text-align: center
  font-size: 18px
  margin: 0px
.minus,.plus
  cursor: pointer
.num
  color: $color_secondary
.bottom
  background-color: $color_back
  width: 100%
  height: 75px
  position: fixed
  // margin: 0 15px 50px 15px
  // margin-bottom: 50px
  // position: absolute
  bottom: 0px
  left: 0px
  right: 0px
  padding-top: 0px
.btn
  border: solid 1px $color_coffee
  padding: 10px 20px
  border-radius: 3px
  cursor: pointer
  width: calc((100% - 30px) / 2 - 5px)
  text-align: center
  position: absolute
  bottom: 0
.btn.canclebtn
  color: $color_coffee
  left: 15px
  bottom: 15px
.btn.savebtn
  background-color: $color_coffee
  color: white
  right: 15px
  bottom: 15px
</style>

<template lang="pug">
.screen
  .page
    .header Cafe Hunter
    .container
      .description 請依據您對咖啡廳各項目的喜好程度給予評分，我們將依據您的喜好尋找最適合您的咖啡廳～
      .remark 1為最不要求，5為最要求
      hr
      .row
        .text 咖啡好喝度:
        .inputbox
          .minus -
          .num 3
          .plus +
      hr
      .row
        .text 安靜要求度:
        .inputbox
          .minus -
          .num 3
          .plus +
      hr
      .row
        .text 價格實惠度:
        .inputbox
          .minus -
          .num 3
          .plus +
      hr
      .row
        .text 插頭便利度:
        .inputbox
          .minus -
          .num 3
          .plus +
      hr
    .bottom
      .btn.canclebtn 取消
      .btn.savebtn 儲存
</template>

<script>

export default {
  data () {
    return {
      "who": "world"
    }
  }
}
</script>
