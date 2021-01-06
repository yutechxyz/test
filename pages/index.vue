<template>
  <div>
    <BaseButton v-bind="buttonProps" @click="handleClick" />
  </div>
</template>

<script>
import BaseButton from '@/components/BaseButton'
export default {
  components: {
    BaseButton
  },
  data() {
    return {
      buttonProps: {
        color: 'success',
        large: false,
        loading: false
      }
    }
  },
  methods: {
    handleClick() {
      console.log('click2')
    }
  }
}
</script>
