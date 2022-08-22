<template>
  <div id="app">
    <ChannelList />
  </div>
</template>

<script>
import ChannelList from '@/components/ChannelList.vue';

export default {
  name: 'App',
  components: {
    ChannelList,
  }
}
</script>

<style>
:root{
  --bg-color-dark: #202225;
  --bg-color-medium: #2F3136;
  --bg-color-light: #36393F;

  --primary-color: #6E86D6;
  --notification-icon-color: #F84A4B;
  --accent-color: #FFA839;
  --text-color: #FFFFF8;
}

*{
  box-sizing: border-box;
}

body{
  font-family: 'Roboto', sans-serif;
}

body, h1, h2, p, ul, li{
  margin: 0px;
  padding: 0px;
}

#app{
  height: 100vh;
  width: 100%;
  display: grid;
  grid-template-columns: 70px 240px 1fr 240px;
  grid-template-rows: 46px 1fr 52px;
  overflow: hidden;
}
</style>
