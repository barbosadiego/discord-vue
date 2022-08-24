<template>
  <div class="mobile-view">
    <div class="superior-bar">
      <span class="material-icons">menu</span>
      <div>
        <span data-v-4525fde0="" class="material-icons">tag</span>
        <h3 data-v-4525fde0="">chat livre</h3>
      </div>
      <div data-v-4525fde0="" class="divider"></div>
      <div data-v-4525fde0="" class="divider"></div>
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
};
</script>

<style lang="scss" scoped>
.mobile-view {
  grid-column: 1/-1;
  grid-row: 1/-1;
  z-index: 20;
  background-color: var(--bg-color-light);
  display: grid;
  padding: 10px;

  .superior-bar{
    display: flex;
  }

  .message-area{
    overflow-y: auto;
  }
}
</style>
