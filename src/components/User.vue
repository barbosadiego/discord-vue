<template>
  <div class="user">
    <div class="avatar">
      <div class="line"></div>
    </div>
    <div class="info">
      <p class="name">Guilherme Rodz</p>
      <p>#2689</p>
    </div>
    <div class="actions">
      <span class="material-icons">mic</span>
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
  grid-row: 3/4;
  grid-column: 2/3;
  margin-top: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
  color: rgba($color: #fff, $alpha: .7);
  background-color: #292B2F;
  z-index: 5;
  padding: 13px 0;

  .avatar{
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background-color: #c4c4c4;
    display: block;
    flex-shrink: 0;
    position: relative;

    .line{
      display: flex;
      align-items: center;
      justify-content: center;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      position: absolute;
      background-color: var(--notification-color);
      bottom: 0px;
      right: 0px;

      &::after{
        content: '';
        display: block;
        width: 6px;
        height: 2px;
        position: absolute;
        background-color: #000;
      }
    }
  }

  .info, .actions{
    display: flex;
  }

  .info{
    flex-direction: column;

    p{
      font-size: 13px;
    }

    .name{
      font-weight: 700;
      color: #fff;
    }
  }

  .actions{
    gap: 5px;
    .material-icons{
      font-size: 15px;
    }
  }
}

</style>