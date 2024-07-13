<template>
  <div>
    <p>
      <a class="btn btn-primary" href="#" @click="toggleCollapse" role="button" :aria-expanded="isOpen">
        collapse me
      </a>
    </p>
    <div class="collapse" :class="{ show: isOpen }">
      <div class="card card-body">
        {{ text }}
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'MyCollapse',
    props: {
      text: {
        type: String,
        required: true,
        default: 'hello'
      },
      opened: {
        type: Boolean,
        default: true
      },
    },
    data() {
      return {
        isOpen: this.opened
      };
    },
    methods: {
      toggleCollapse() {
        this.isOpen = !this.isOpen;
      }
    }
  }
</script>

<style scoped>

</style>