<script setup>

defineProps({
  title: {
    type: String,
    required: Boolean
  },
  text: {
    type: String,
    required: Boolean
  }
})
</script>

<template>
  <div className="card">
   <div className="card-body">
     <h4 v-if="title" className="card-title card">11111{{ title }}</h4>
     <p v-if="text" className="card-text">2222{{ text }}</p>
   </div>
  </div>
</template>

<style scoped>

</style>
