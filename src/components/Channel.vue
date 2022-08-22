<template>
  <div 
    class="channel" 
    :class="{'isActive' : isActive, 'hasNotification' : hasNotification, 'chat' : chat}"
  >
    <img class="icon" v-if="isActive" src="@/assets/discord.svg" alt="">
  </div>
</template>

<script>
export default {
  name: 'ChannelIcon',
  props:{
    isActive: Boolean,
    hasNotification: Boolean,
    chat: Boolean,
  }
}
</script>

<style lang="scss" scoped>
.channel{
  height: 48px;
  width: 48px;
  border-radius: 50%;
  background-color: #36393F;
  position: relative;
  flex-shrink: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;

  &.isActive{
    background-color: var(--primary-color);
    border-radius: 16px;
  }

  &.hasNotification::after{
    content: '';
    display: block;
    width: 16px;
    height: 16px;
    position: absolute;
    background-color: var(--notification-color);
    border-radius: 50%;
    box-shadow: 0 0 0 4px var(--bg-color-dark);
    bottom: 0px;
    right: 0px;
  }

  &.chat::before{
    content: '';
    display: block;
    width: 9px;
    height: 9px;
    border-radius: 50%;
    position: absolute;
    background-color: #fff;
    left: -16px;
  }

  .icon{
    width: 26px;
  }
}
</style>