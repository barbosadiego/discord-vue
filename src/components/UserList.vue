<template>
  <div class="user-list">
    <div class="online">
      <span>DISPONÍVEL - 1</span>
      <Avatar name="Guilherme Rodz"/>
    </div>
    <div class="offline">
      <span>OFFLINE - 18</span>
      <Avatar name="Diego Fernandes"/>
      <Avatar name="Fulano" v-for="item in 18" :key="item.id"/>
    </div>
  </div>
</template>

<script>
import Avatar from '@/components/Avatar.vue';

export default {
  name: 'UserList',
  components:{
    Avatar,
  }
}
</script>

<style lang="scss" scoped>
.user-list{
  grid-column: 4/5;
  grid-row: 2/4;
  background-color: var(--bg-color-medium);
  padding: 23px 16px;
}
</style>