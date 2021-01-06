<template>
  <div>
    <BaseButton v-bind="buttonProps" @click="handleClick" />
    <v-row class="blue lighten-4" style="height: 450px;" justify="center" align-content="center">
      <v-col cols=12 sm=10 md=8 lg=4 xl=3 v-for="n in 3" :key="n">
        <v-card color="blue" outlined tile height=150></v-card>
      </v-col>
    </v-row>
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
