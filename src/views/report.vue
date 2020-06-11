<template>
  <div class="report">
    <img class="banner"
         src="../assets/ban.jpg"
         alt="">
    <div class="list">
      <van-tabs type="card">
        <van-tab title="订餐报表">

        </van-tab>
        <van-tab title="订餐详情">订餐详情</van-tab>
      </van-tabs>
    </div>
  </div>
</template>

<style scoped>
.report {
  height: 100%;
  background: #008f7b;
}
.list {
  box-sizing: border-box;
  height: calc(100vh - 17.65rem - 1.25rem);
  padding-top: 2.5rem;
  margin: 0 1rem;
  background: #fff;
  border-radius: 9px;
}
</style>