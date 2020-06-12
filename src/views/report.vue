<template>
  <div class="report">
    <img class="banner"
         src="../assets/ban.jpg"
         alt="">
    <div class="list">
      <van-tabs type="card">
        <van-tab title="订餐报表">
          <ul class="food-sum-list">
            <li><span>预定餐品</span><span>数量</span></li>
            <li><span>套餐</span><span>1份</span></li>
            <li><span>水饺</span><span>2份</span></li>
            <li><span>面条</span><span>3份</span></li>
            <li><span>砂锅</span><span>4份</span></li>
          </ul>
          <div class="food-sum">共9份餐品</div>
        </van-tab>
        <van-tab title="订餐详情">
          <ul class="food-details">
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
            <li><span>张某某 网络部 &nbsp; 6/10</span><span>套餐1份 砂锅4份</span></li>
          </ul>
        </van-tab>
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
  overflow: hidden;
  height: calc(100vh - 17.65rem - 1.25rem);
  padding-top: 2.5rem;
  margin: 0 1rem;
  background: #fff;
  border-radius: 9px;
}
.food-sum-list {
  margin: 1.6rem 0.8rem 0;
  padding-bottom: 1rem;
  border-bottom: 1px solid #dedede;
}
.food-sum-list li {
  display: flex;
  justify-content: space-between;
  padding: 0.9rem 2.3rem 0.9rem 2.4rem;
}
.food-sum-list li:first-child {
  font-weight: bold;
}
.food-sum {
  text-align: right;
  padding: 1.5rem 2.5rem;
  font-size: 1.2rem;
}

.food-details {
  max-height: calc(100vh - 26.15rem);
  margin: 1.5rem 0 0.7rem;
  overflow-y: scroll;
}
.food-details li {
  display: flex;
  justify-content: space-between;
  height: 2.5rem;
  line-height: 2.5rem;
  padding: 0 1.3rem;
  font-size: 1rem;
}
.food-details li:nth-child(odd) {
  background: #eee;
}
.food-details span:first-child {
  color: #008f7b;
}
</style>
<style>
.van-tabs--card > .van-tabs__wrap,
.van-tabs__nav--card {
  height: 3.25rem;
}
.van-tabs__nav--card {
  border: 0;
}
.van-tabs__nav--card .van-tab {
  margin: 0 0.5rem;
  color: #008f7b;
  border: 1px solid #008f7b;
  border-radius: 0.5rem;
  font-size: 1.3rem;
}
.van-tabs__nav--card .van-tab.van-tab--active {
  color: #fff;
  background-color: #008f7b;
}
.van-tabs__nav--card .van-tab:last-child {
  border-right: 1px solid #008f7b;
}
</style>