<template>
  <div>
    {{ name + ": " + level }}
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    level: Number,
    categories: Array
  },
  computed: {
    colored() {
      return (this.level > 50);
    }
  }
}
</script>