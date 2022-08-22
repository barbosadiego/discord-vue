<template>
  <div class="channel-list">
    <Channel isActive icon="@/assets/discord.svg" />
    <Channel v-for="channel, index in 12" :key="index" />
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
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  padding: 10px 0px;
  //hide scrollbar but allow scrolling
  -ms-overflow-style: none; //edge
  scrollbar-width: none; //firefox
  // safari, chrome, opera
  &::-webkit-scrollbar{
    display: none
  };
}
</style>
