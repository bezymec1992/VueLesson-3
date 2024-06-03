<template>
  <AlertVue :type="type"  :text="text"/>;
</template>

<script>
import AlertVue from './components/AlertVue.vue'

export default {
  name: 'App',
  data() {
    return {
      text: 'What is love?',
      type: 'warning'
    }
  },
  components: {
    AlertVue
  }
}
</script>

<style>

</style>
