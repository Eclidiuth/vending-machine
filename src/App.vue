<template>
  <div id="app">
    <h1>Vending Machine</h1>
    <vm-row :buttonLength="10" :startFrom="0" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="1" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="2" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="3" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="5" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="6" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="7" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="8" :lightUpLength="4"/>
  </div>
</template>

<script>
import VMRow from '@/components/VMRow.vue'

export default {
  name: 'App',
  components: {
    'vm-row': VMRow
  }
}
</script>

<style lang="scss" scoped>
#app {
  margin: 0 auto;
  width: 80%;

  h1 {
    font-weight: 400;
    font-size: 2.5rem;
  }
}
</style>