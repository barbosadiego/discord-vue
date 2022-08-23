<template>
  <div class="message">
    <div class="avatar"></div>
    <div class="data">
      <h3 class="user">Guilherme Rodz <span>12/06/2022</span></h3>
      <p>
        <slot></slot>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MessageComponent',
};
</script>

<style lang="scss" scoped>
.message {
  color: var(--text-color);
  display: flex;
  gap: 17px;
  padding: 22px 16px;

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
}
</style>
