<template>
  <span :class="[shouldLightUp ? 'active' : '']">
    <slot />
  </span>
</template>

<script>
export default {
  name: 'VMButton',
  props: {
    shouldLightUp: Boolean
  }
}
</script>

<style lang="scss" scoped>
span {
  background: #252525;
  color: #ffffff;
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;
  font-size: 0.875rem;
  padding: 1rem 0;

  &::before {
    background: #777777;
    border-radius: 50%;
    content: '';
    display: block;
    position: relative;
    top: 2px;
    margin: 0 8px;
    width: 12px;
    height: 12px;
  }

  &:hover {
    background: #303030;
  }
  
  &.active::before {
    background: red;
  }
}
</style>