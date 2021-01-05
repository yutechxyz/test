<template>
  <div>
    <v-btn
      :x-large="false"
      depressed
      :color="color"
      :disabled="false"
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
    size: { default: 'x-large' }
  },
  methods: {
    handleClick() {
      console.log('click')
    }
  }
}
</script>
