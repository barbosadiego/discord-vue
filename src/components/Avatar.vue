<template>
  <div class="avatar" :class="{ 'isBot' : isBot }">
    <div class="icon"></div>
    <h3>{{ name }}</h3>
  </div>
</template>

<script>
export default {
  name: 'AvatarComponent',
  props:{
    name: String,
    isBot: Boolean,
  }
}
</script>

<style lang="scss" scoped>
.avatar{
  display: flex;
  align-items: center;
  gap: 13px;
  margin-bottom: 11px;
  color: rgba($color: #fff, $alpha: .7);
  cursor: pointer;

  .icon{
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background-color: var(--bg-color-light);
  }

  h3{
    font-weight: 400;
    font-size: 1rem;
    line-height: 19px;
  }

  &.isBot{
    .icon{
      background-color: var(--accent-color);
    }
    h3::after{
      content: 'BOT';
      display: inline-grid;
      place-items: center;
      width: 28px;
      height: 15px;
      border-radius: 4px;
      background-color: var(--primary-color);
      font-size: 9px;
      font-weight: 700;
      margin-left: 10px;
    }
  }
}
</style>