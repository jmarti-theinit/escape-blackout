<template>
  <div class="desktop-icon">
    <img :data-test-id="`desktop-icon-clickable-${text}`" :src="icon" :alt="text" @click="$emit('click')"/>
    <div class="desktop-icon__text">{{ text }}</div>
  </div>
</template>
<style scoped>
.desktop-icon {
  text-align: center;
  width: 8vw;
}
img {
  width: 7vw;
  height: auto;
}
.desktop-icon__text {
  font-size: 2vw;
}
</style>
<script>
export default {
  name: 'desktop-icon',
  props: {
    text: {
      type: String,
      default: ''
    },
    icon: {
      type: String,
      default: ''
    }
  }
};
</script>
