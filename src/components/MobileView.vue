<template>
  <div class="mobile-view">
    <div class="superior-bar">
      <span class="material-icons menu" @click="toggleMenu">menu</span>
      <div class="server-title">
        <span data-v-4525fde0="" class="material-icons">tag</span>
        <h3 data-v-4525fde0="">chat livre</h3>
        <div data-v-4525fde0="" class="divider"></div>
        <p data-v-4525fde0="">Canal aberto para conversas</p>
      </div>
      <span class="material-icons group">group</span>
    </div>
    <div class="message-area">
      <Message
        v-for="item in 17"
        :key="item.id"
        user="Guilherme Rodz"
        text="Isso é uma mensagem"
      />
    </div>
  </div>
</template>

<script>
import Message from '@/components/Message.vue';

export default {
  name: 'MobileView',
  components: {
    Message,
  },
  methods: {
    toggleMenu() {
      this.$emit('changeView');
    },
  },
};
</script>

<style lang="scss" scoped>
.mobile-view {
  grid-column: 1/-1;
  grid-row: 1/-1;
  background-color: var(--bg-color-light);
  display: grid;

  .superior-bar {
    padding: 16px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 10px;
    color: rgba($color: #fff, $alpha: 0.7);

    .menu,
    .group {
      cursor: pointer;
    }

    .server-title {
      flex: 1;
      display: flex;
      align-items: center;
      gap: 7px;
      margin-left: 7px;

      h3 {
        font-size: 14px;
        line-height: 16px;
      }

      .divider {
        width: 2px;
        height: 24px;
        display: block;
        background-color: #42454b;
      }
    }

    p {
      width: 15ch;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      font-size: 14px;
    }
  }

  .message-area {
    overflow-y: auto;
  }
}
</style>
