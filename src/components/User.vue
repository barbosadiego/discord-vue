<template>
  <div class="user">
    <div class="avatar"></div>
    <div class="info">
      <p>Guilherme Rodz</p>
      <p>#2689</p>
    </div>
    <div class="actions">
      <span class="material-icons">microfone</span>
      <span class="material-icons">headphones</span>
      <span class="material-icons">settings</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserComponent'
}
</script>

<style lang="scss" scoped>
.user{
  margin-top: auto;
  display: flex;

  .avatar{
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background-color: #c4c4c4;
    display: block;
  }
}

</style>