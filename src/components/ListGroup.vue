<template>
  <ul class="list-group">
    <template v-for="(child, index) in $slots.default()" :key="index">
      <li class="list-group-item">
        <component :is="child" />
      </li>
    </template>
  </ul>
</template>

<script>
  export default {
    name: 'ListGroup'
  }
</script>

<style scoped>

</style>