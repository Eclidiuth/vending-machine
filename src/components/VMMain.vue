<template>
  <div>
    <vm-row :buttonLength="10" :startFrom="0" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="1" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="2" :lightUpLength="4"/>
    <vm-row :buttonLength="10" :startFrom="3" :lightUpLength="4"/>
  </div>
</template>

<script>
import VMRow from '@/components/VMRow.vue'

export default {
  name: 'VMMain',
  components: {
    'vm-row': VMRow
  },
}
</script>