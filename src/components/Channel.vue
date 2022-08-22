<template>
  <div class="channel" :class="{'isActive' : isActive}">
    <img v-if="icon" :src="icon" alt="">
  </div>
</template>

<script>
export default {
  name: 'ChannelIcon',
  props:{
    isActive: Boolean,
    icon: String,
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

  &.isActive{
    background-color: var(--primary-color);
    border-radius: 16px;
  }
}
</style>