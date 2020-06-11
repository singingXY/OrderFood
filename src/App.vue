<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "app"
};
</script>
<style>
#app {
  width: 100%;
  max-width: 750px;
  margin: 0 auto;
  color: #333;
  font-size: 1.2rem;
}
</style>