<template>
  <div class="chat-area">
    <div class="message-area">
      <Message 
        v-for="item in 17" 
        :key="item.id" 
        user="Guilherme Rodz" 
        text="Isso é uma mensagem"
      />
      <Message 
        isAtual
        isBot
        user="Diego Fernandes" 
        text="@Guilherme Rodz, me carrega no LoL e CS de novo por favor?"
      />
    </div>
    <div class="input-area">
      <span class="material-icons">alternate_email</span>
      <input 
        type="text" 
        placeholder="Conversar em #chat-livre" 
      />
    </div>
  </div>
</template>

<script>
import Message from '@/components/Message.vue';

export default {
  name: 'ChatArea',
  components: {
    Message,
  },
  methods:{
    scroll(){
      const el = document.querySelector('.message-area');
      el.scrollTo({
        top: 500,
        behavior: 'smooth'
      })
    }
  },
  mounted(){
    this.scroll()
  }
};
</script>

<style lang="scss" scoped>
.chat-area {
  grid-row: 2/4;
  grid-column: 3/4;
  background-color: var(--bg-color-light);
  position: relative;
  color: rgba($color: #000000, $alpha: 0.7);
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr 90px;

  .message-area{
    overflow-y: auto;
    flex: 1;

    //chrome, safari and edge
    &::-webkit-scrollbar{
      width: 8px;
      background-color: #2F3136;
    }

    //chrome, safari and edge
    &::-webkit-scrollbar-thumb{
      background-color: #000000;
      border-radius: 4px;
    }
  }

  .input-area {
    display: flex;
    align-items: center;
    padding-inline: 16px;
    padding-top: 20px;
    padding-bottom: 23px;
    z-index: 5;
    background-color: var(--bg-color-light);

    input {
      background-color: #40444b;
      padding: 12px;
      border: none;
      border-radius: 7px;
      color: var(--text-color);
      font-size: 1rem;
      padding-left: 40px;
      outline: none;
      width: 100%;

      &::placeholder {
        font-size: 16px;
      }

      &:focus {
        box-shadow: 0 0 0 2px var(--accent-color);
      }
    }

    .material-icons {
      color: #7a7c80;
      position: absolute;
      left: 25px;
    }
  }
}
</style>
