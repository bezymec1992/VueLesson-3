<template>
  <AlertVue :type="type"  :text="text"/>
  <BtnGroup />
  <ListGroup>
    <p>one</p>
    <p>two</p>
  </ListGroup>
  <MyCollapse text="це прихований текст" :opened="true"/>

  <MySlider :slides="slides"/>

</template>

<script>
import AlertVue from './components/AlertVue.vue'
import BtnGroup from './components/BtnGroup.vue'
import ListGroup from './components/ListGroup.vue'
import MyCollapse from './components/Collapse.vue'
import MySlider from './components/MySlider.vue'

export default {
  name: 'App',
  data() {
    return {
      text: 'What is love?asasdas',
      type: 'warning',
      slides: [
          { src: require('./assets/img/1.jpeg'), alt: 'First slide' },
          { src: require('./assets/img/2.png'), alt: 'Second slide' },
          { src: require('./assets/img/3.png'), alt: 'Third slide' }
        ]
    }
  },
  components: {
    AlertVue,
    BtnGroup,
    ListGroup,
    MyCollapse,
    MySlider
  }
}
</script>

<style>

</style>
