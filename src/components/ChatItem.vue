<template>
  <div class="chat-list" :class="{'active' : active}">
    <div class="chat-channel">
      <div>
        <span class="material-icons">tag</span>
        <p>{{ title }}</p>
      </div>
      <div>
        <span class="material-icons">person_add</span>
        <span class="material-icons cog">settings</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChatItem',
  props: {
    title: String,
    active: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.chat-list {
  color: rgba($color: #ffffff, $alpha: 0.5);
  padding: 13px 16px;
  width: 100%;
  transition: .3s;
  cursor: pointer;

  .chat-channel {
    display: flex;
    justify-content: space-between;
    align-items: center;

    & div:first-child {
      display: flex;
      align-items: center;
      gap: 9px;
    }

    p {
      font-weight: 400;
      font-size: 18px;
      line-height: 17px;
    }

    .material-icons {
      font-size: 1.2rem;
    }

    .cog {
      margin-left: 7px;
    }
  }

  &:hover,
  &.active {
    background-color: var(--bg-color-light);
  }
}
</style>
