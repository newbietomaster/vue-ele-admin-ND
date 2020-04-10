<template>
  <div class="setH">
    <span>{{ titleName }}</span>
  </div>
</template>
<script>
export default {
  props: {
    titleName: {
      type: String,
      default: ''
    }
  }
}
</script>
<style scoped>
.setH {
    display: block;
    font-size: 20px;
    font-weight: bold;
    color:#000000;
}
</style>
