<template>
  <div class="channel-list">
    <div v-for="channel, index in 50" :key="index">
      <Channel />
    </div>
  </div>
</template>

<script>
import Channel from '@/components/Channel.vue';

export default {
  name: 'ChannelList',
  components: {
    Channel,
  },
};
</script>

<style lang="scss" scoped>
.channel-list {
  background-color: var(--bg-color-dark);
  grid-row: 1/-1;
  overflow-y: scroll;
}
</style>
