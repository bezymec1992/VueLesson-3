<template>
  <div class="btn-group">
    <button type="button"
      :class="['btn', 'btn-secondary', 'left', activeBtn === 'left' ? 'active' : '']"
      @click="setActive('left')"
    >
      Button 1
    </button>
    <button type="button"
      :class="['btn', 'btn-secondary', 'right', activeBtn === 'right' ? 'active' : '']"
      @click="setActive('right')"
    >
      Button 2
    </button>
  </div>
</template>

<script>
export default {
  name: 'BtnGroup',
  data() {
    return {
      activeBtn: null,
    };
  },
  methods: {
    setActive(btn) {
      this.activeBtn = btn
    }
  }
}

</script>

<style scoped>
 
</style>