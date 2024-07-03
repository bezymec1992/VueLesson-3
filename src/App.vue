<template>
  <AlertVue :type="type"  :text="text"/>
  <BtnGroup />
</template>

<script>
import AlertVue from './components/AlertVue.vue'
import BtnGroup from './components/BtnGroup.vue'

export default {
  name: 'App',
  data() {
    return {
      text: 'What is love?asasdas',
      type: 'warning'
    }
  },
  components: {
    AlertVue,
    BtnGroup
  }
}
</script>

<style>

</style>
