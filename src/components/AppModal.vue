<template>
  <div class="modal-backdrop" @click="$emit('close')"></div>
  <div class="modal">
    <h3>Certificates</h3>
    <div v-for="item in certificates" :key="item">
      {{ item }}
    </div>
  </div>
</template>

<script>
export default {
  emits: ['close'],
  data() {
    return {
      certificates: [1, 2, 3]
    }
  }
}
</script>

<style lang="scss">
body {
  .modal {
    background: rgba(0, 0, 0, 0.432);
    color: #fff;
  }
}
</style>