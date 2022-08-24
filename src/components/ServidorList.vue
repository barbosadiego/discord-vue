<template>
  <div class="servidor-list">
    <div class="selector">
      <h1>Servidor do Rodz</h1>
      <span class="material-icons arrow">expand_more</span>
    </div>
    <div class="title">
      <h2>canais de texto</h2>
      <span class="material-icons add">add</span>
    </div>
    <ChatItem title="chat-livre" active/>
    <ChatItem title="trabalho" />
    <ChatItem title="lolzinho" />
    <ChatItem title="valorant" />
    <ChatItem title="csgo" />
    <User />
  </div>
</template>

<script>
import ChatItem from '@/components/ChatItem.vue';
import User from '@/components/User.vue';

export default {
  name: 'ServidorList',
  components: {
    ChatItem,
    User,
  },
};
</script>

<style lang="scss" scoped>
.servidor-list {
  background-color: var(--bg-color-medium);
  grid-row: 1/-1;
  display: flex;
  flex-direction: column;
  @media (max-width:900px){
    grid-column: 2/3;
  }

  .selector {
    display: flex;
    justify-content: space-between;
    padding: 11px 16px;
    align-items: center;
    color: var(--text-color);
    box-shadow: 0 1px 2px rgba($color: #000000, $alpha: 0.5);
    cursor: pointer;
  }

  .title {
    color: rgba($color: #ffffff, $alpha: 0.5);
    padding: 13px 16px;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .add{
      cursor: pointer;
    }
  }
}
</style>
