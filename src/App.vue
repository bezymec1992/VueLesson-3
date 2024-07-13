<template>
  <AlertVue :type="type"  :text="text"/>
  <BtnGroup />

  <ListGroup>
    <p>one</p>
    <p>two</p>
  </ListGroup>

  <MyCollapse text="це прихований текст" :opened="true"/>

</template>

<script>
import AlertVue from './components/AlertVue.vue'
import BtnGroup from './components/BtnGroup.vue'
import ListGroup from './components/ListGroup.vue'
import MyCollapse from './components/Collapse.vue'

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
    ListGroup,
    MyCollapse
  }
}
</script>

<style>

</style>
