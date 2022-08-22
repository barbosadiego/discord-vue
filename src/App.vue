<template>
  <div id="app">
    <ChannelList />
    <ServidorList />
  </div>
</template>

<script>
import ChannelList from '@/components/ChannelList.vue';
import ServidorList from '@/components/ServidorList.vue';

export default {
  name: 'App',
  components: {
    ChannelList,
    ServidorList,
  }
}
</script>

<style>
:root{
  --bg-color-dark: #202225;
  --bg-color-medium: #2F3136;
  --bg-color-light: #36393F;

  --primary-color: #6E86D6;
  --notification-color: #F84A4B;
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

h1{
  font-weight: 700;
  font-size: 1rem;
  line-height: 19px;
  color: var(--text-color);
}

h2{
  font-weight: 500;
  font-size: 14px;
  line-height: 14px;
  text-transform: uppercase;
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
