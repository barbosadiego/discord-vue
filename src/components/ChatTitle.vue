<template>
  <div class="chat-title">
    <div>
      <span class="material-icons">tag</span>
      <h3>chat livre</h3>
    </div>
    <div class="divider"></div>
    <p>Canal aberto para conversas</p>
  </div>
</template>

<script>
export default {
  name: 'ChatTitle',

}
</script>

<style lang="scss" scoped>
.chat-title{
  z-index: 5;
  grid-row: 1;
  grid-column: 3/5;
  background-color: var(--bg-color-light);
  display: flex;
  align-items: center;
  padding-inline: 17px;
  color: rgba($color: #ffffff, $alpha: .5);
  box-shadow: 0 1px 2px rgba($color: #000000, $alpha: .5);
  @media (max-width:900px){
    display: none;
  }

  div{
    display: flex;
    gap: 9px;
    align-items: center;
    margin-right: 13px;

    h3{
      color: var(--text-color);
      text-transform: unset;
    }
  }

  .divider{
    width: 1px;
    height: 24px;
    display: block;
    background-color: #42454B;
  }
}
</style>