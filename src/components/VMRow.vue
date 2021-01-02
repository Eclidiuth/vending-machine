<template>
  <div class="vm-row">
    <vm-button v-for="(button, index) in buttonState" :key="index" :shouldLightUp="button">Buy</vm-button>
  </div>
</template>

<script>
import VMButton from '@/components/VMButton.vue'

export default {
  name: 'VMRow',
  components: {
    'vm-button': VMButton
  },
  props: {
    buttonLength : Number,
    startFrom    : Number,
    lightUpLength: Number
  },
  data(){
    return {
      count: this.startFrom
    }
  },
  computed: {
    buttonState(){
      const buttonState = Array(this.buttonLength).fill(false)
      const lightUpLength = this.lightUpLength

      if(this.count <= this.buttonLength - 1){
        for(let i = 0; i < lightUpLength; i++){
          if(this.count - i >= 0){
            buttonState[this.count - i] = true
          }
        }
      } else if(this.count <= (this.buttonLength - 1) + (this.lightUpLength - 1)){
        // 8 3
        // 9 2
        // 10 1
        const lightUpLength = (this.buttonLength - 1) + this.lightUpLength - this.count
        for(let i = 0; i < lightUpLength ; i++){
          buttonState[(this. buttonLength - 1) - i] = true
        }
      }

      return buttonState
    }
  },
  created(){
    setInterval(() => {
      this.count++

      if(this.count == this.buttonLength + this.lightUpLength){
        this.count = 0
      }
    }, 500)
  }
}
</script>

<style lang="scss" scoped>
.vm-row {
  display: flex;
}
</style>