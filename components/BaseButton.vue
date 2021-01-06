<template>
  <VBtn
    :color="color"
    :elevation="2"
    :large="large"
    :loading="loading"
    @click="handleClick"
  >
    Extra large Button
  </VBtn>
</template>

<script>
export default {
  props: {
    color: { default: 'warning' },
    large: { default: false },
    loading: { default: false }
  },
  methods: {
    handleClick() {
      this.$emit('click')
    }
  }
}
</script>