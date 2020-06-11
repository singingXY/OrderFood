<template>
  <div class="login">
    <img class="banner"
         src="../assets/ban.jpg"
         alt="">
    <h2>在线订餐</h2>
    <div class="form">
      <label for=""
             @click="menuHide()">
        <span>预订餐品</span>
        <input type="text"
               placeholder="请选择餐品">
      </label>
      <label for="">
        <span>手机号码</span>
        <input type="text"
               placeholder="请输入手机号">
      </label>
      <label for="">
        <span>验证码</span>
        <input type="text"
               placeholder="请输入短信验证码">
        <div class="code-btn">获取验证码</div>
      </label>
      <label for="">
        <span>就餐日期</span>
        <input type="date">
      </label>
    </div>
    <div class="bottom">
      <div class="shoppingCart"
           @click="menuHide()">
        <span>{{foodSum}}</span>
        <img src="../assets/cart.png"
             alt="">
      </div>
      <p>请到食堂刷卡取餐</p>
      <div class="submit">立即提交</div>
    </div>
    <van-action-sheet v-model="menuShow"
                      :round="false">
      <div class="delete"
           @click="clearNum">
        <span>
          <van-icon name="delete" />清除重选</span>
      </div>
      <div class="menu-content">
        <van-cell v-for="(menus,index) in menu"
                  :key="index"
                  :title="menus.text">
          <template #right-icon>
            <van-stepper v-model="menus.num"
                         theme="round"
                         min="0"
                         button-size="22"
                         disable-input
                         default-value="0" />
          </template>
        </van-cell>
      </div>
    </van-action-sheet>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      menuShow: true,
      menu: [
        { text: "套餐", num: 0 },
        { text: "炒饭", num: 0 },
        { text: "砂锅", num: 0 },
        { text: "水饺", num: 0 },
        { text: "面条", num: 0 }
      ]
    };
  },
  computed: {
    foodSum: function() {
      let sum = 0;
      for (let i = 0; i < this.menu.length; i++) {
        sum += this.menu[i].num;
      }
      return sum;
    }
  },
  methods: {
    clearNum() {
      for (let i = 0; i < this.menu.length; i++) {
        this.menu[i].num = 0;
      }
    },
    menuHide() {
      this.menuShow = !this.menuShow;
    }
  }
};
</script>

<style scoped>
.banner {
  width: 100%;
}
h2 {
  position: relative;
  font-size: 2.25rem;
  font-weight: 700;
  color: #008f7b;
  text-align: center;
  padding: 0.8rem 0;
  margin-top: 2.5rem;
}
h2::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 50%;
  display: block;
  margin-left: -2.5rem;
  width: 5rem;
  height: 3px;
  background: #008f7b;
}
.form {
  width: 87.5%;
  margin: 2rem auto 0;
}
.form label {
  position: relative;
  box-sizing: border-box;
  display: block;
  margin-bottom: 1rem;
  width: 100%;
  padding: 1.1rem 2.1rem;
  border: solid 1px #008f7b;
  border-radius: 3rem;
  line-height: 2.25rem;
}
.form span {
  display: inline-block;
  width: 6.3rem;
  font-size: 1.3rem;
  border-right: 1px solid #c9c9c9;
}
.form input {
  text-indent: 1.3rem;
}
.code-btn {
  position: absolute;
  right: 1rem;
  top: 1.1rem;
  width: 6rem;
  height: 2.35rem;
  line-height: 2.35rem;
  background: #008f7b;
  font-size: 0.9rem;
  color: #fff;
  text-align: center;
  border-radius: 4px;
}
.bottom {
  box-sizing: border-box;
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 4.5rem;
  padding: 1.6rem 0;
  background: #4f4f4f;
  z-index: 20000;
}
.bottom p {
  box-sizing: border-box;
  position: absolute;
  top: 0;
  left: 24.7%;
  height: 4.5rem;
  padding: 1.6rem 0;
  color: #fff;
  font-size: 1rem;
}
.bottom .submit {
  box-sizing: border-box;
  position: absolute;
  top: 0;
  right: 0;
  width: 26.5%;
  height: 4.5rem;
  padding: 1.6rem 0;
  text-align: center;
  font-size: 1.3rem;
  font-weight: 700;
  background: #fdcc59;
}
.shoppingCart {
  position: absolute;
  left: 1rem;
  bottom: 0.9rem;
}
.shoppingCart span {
  position: absolute;
  right: 5px;
  top: -5px;
  display: block;
  width: 1.5rem;
  height: 1.5rem;
  line-height: 1.5rem;
  text-align: center;
  background: #fc3604;
  color: #fff;
  border-radius: 50%;
  font-size: 1.1rem;
}
.shoppingCart img {
  width: 5rem;
}
.delete {
  overflow: hidden;
  padding: 0.7rem 0;
  background: #f4f4f4;
}
.delete span {
  margin-right: 1.5rem;
  float: right;
  font-size: 0.9rem;
  line-height: 1;
}
.delete .van-icon-delete {
  font-size: 1.3rem;
  margin-right: 0.4rem;
  vertical-align: text-bottom;
}
.van-cell__title {
  font-size: 1.3rem;
}
.menu-content {
  height: 11.9rem;
  margin-bottom: 2.35rem;
  overflow-y: scroll;
}
.van-popup--bottom {
  bottom: 4.5rem;
}
</style>
