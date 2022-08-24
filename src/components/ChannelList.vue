<template>
  <div class="channel-list">
    <Channel isActive hasNotification @click.native="toggleView"/>
    <div class="divider"></div>
    <Channel v-for="channel, index in 4" :key="index" chat/>
    <Channel hasNotification/>
    <Channel v-for="channel, index in 7" :key="index + 5" />
  </div>
</template>

<script>
import Channel from '@/components/Channel.vue';

export default {
  name: 'ChannelList',
  components: {
    Channel,
  },
  methods:{
    toggleView(){
      this.$emit('toggleView')
    }
  }
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

  @media (max-width:900px){
    grid-column: 1/2;
  }

  .divider{
    width: 32px;
    height: 2px;
    background-color: var(--bg-color-medium);
  }
}
</style>
