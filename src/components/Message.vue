<template>
  <div class="message" :class="{ 'isAtual': isAtual, 'isBot' : isBot }">
    <div class="avatar"></div>
    <div class="data">
      <h3 class="user">{{ user }} <span>12/06/2022</span></h3>
      <p> {{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MessageComponent',
  props: {
    isAtual: Boolean,
    text: String,
    user: String,
    isBot: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.message {
  color: var(--text-color);
  display: flex;
  gap: 17px;
  padding: 6px 16px;
  margin: 15px 0px;

  .avatar {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: var(--bg-color-medium);
  }

  .data {
    .user {
      font-size: 16px;
      font-weight: 500;
      line-height: 19px;

      span {
        color: rgba($color: #fff, $alpha: 0.42);
        font-size: 13px;
        font-weight: 400;
        margin-left: 6px;
      }
    }
  }

  &.isAtual {
    background-color: #413f3f;
    border-left: 2px solid var(--accent-color);

    .avatar{
      background-color: var(--accent-color);
    }
  }

  &.isBot{
    .data .user {
      display: flex;
      align-items: center;
      gap: 11px;

      &::after{
        content: 'BOT';
        display: inline-grid;
        place-items: center;
        width: 28px;
        height: 15px;
        border-radius: 4px;
        background-color: var(--primary-color);
        font-size: 9px;
        line-height: 10px;
      }
      
      span{
        display: none;
      }
    }
  }
}
</style>
