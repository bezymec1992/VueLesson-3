<template>
  <div :class="'alert alert-' + type" role="alert">{{ text }}</div>
</template>

<script>
export default {
  name: 'AlertVue',
  props: {
    text: {
      type: String,
      required:true
    },
    type: {
      type: String,
      default: "danger"
    }
    
  }
}

</script>

<style scoped>
 
</style>
