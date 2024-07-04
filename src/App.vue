<template>
  <AlertVue :type="type"  :text="text"/>
  <BtnGroup />

  <ListGroup>
    <p>one</p>
    <p>two</p>
  </ListGroup>

</template>

<script>
import AlertVue from './components/AlertVue.vue'
import BtnGroup from './components/BtnGroup.vue'
import ListGroup from './components/ListGroup.vue'

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
    BtnGroup,
    ListGroup
  }
}
</script>

<style>

</style>
