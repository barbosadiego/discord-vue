<template>
  <div class="user-list">
    <div class="online">
      <span>DISPONÍVEL - 1</span>
      
    </div>
    <div class="offline">
      <span>OFFLINE - 18</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserList',
}
</script>

<style lang="scss" scoped>
.user-list{
  grid-column: 4/5;
  grid-row: 2/4;
  background-color: var(--bg-color-medium);
}
</style>