<template>
  <transition-group name="slide-down" appear>
    <div
      v-for="error in errors"
      :key="error"
      class="fvl-checkbox-error-message"
      v-html="multible + error"
    />
  </transition-group>
</template>

<script>
    export default {
        props: {
            errors: {
                type: Array,
                default: () => []
            }
        },
        computed: {
            multible() {
                return this.errors.length > 1 ? '- ' : ''
            }
        }
    }
</script>
