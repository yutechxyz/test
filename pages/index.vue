<template>
  <div>
    <v-btn
      :color="color"
      :elevation="2"
      :large="large"
      :loading="loading"
      @click="handleClick"
    >
      Extra large Button
    </v-btn>
  </div>
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
      console.log('click')
    }
  }
}
</script>
