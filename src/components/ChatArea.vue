<template>
  <div class="chat-area">
    <div class="input-area">
      <span class="material-icons">alternate_email</span>
      <input type="text" placeholder="Conversar em #chat-livre" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChatArea',
};
</script>

<style lang="scss" scoped>
.chat-area {
  grid-row: 2/4;
  grid-column: 3/4;
  background-color: var(--bg-color-light);
  position: relative;
  color: rgba($color: #000000, $alpha: 0.7);

  .input-area {
    display: flex;
    align-items: center;
    padding-inline: 16px;
    padding-top: 20px;
    padding-bottom: 23px;
    position: absolute;
    bottom: 0px;
    width: 100%;
    margin-inline: auto;

    input {
      background-color: #40444b;
      padding: 12px;
      flex: 1;
      border: none;
      border-radius: 7px;
      color: var(--text-color);
      font-size: 1rem;
      padding-left: 40px;
      outline: none;

      &::placeholder {
        font-size: 16px;
      }

      &:focus{
        box-shadow: 0 0 0 2px var(--accent-color);
      }
    }

    .material-icons {
      color: #7A7C80;
      position: absolute;
      left: 25px;
    }
  }
}
</style>
