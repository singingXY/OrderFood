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
  height: 100%;
  max-width: 750px;
  margin: 0 auto;
  color: #333;
  font-size: 1.2rem;
}

.banner {
  width: 100%;
}
</style>