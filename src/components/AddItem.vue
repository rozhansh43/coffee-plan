<template>
  <div>
    <form @submit.prevent="emitAdd">
      <input v-model="name">

      <button type="submit">
        Add
      </button>
    </form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      name: null
    }
  },
  methods: {
    emitAdd () {
       this.$emit('add', this.name)
       this.name = null
    }
  }
}
</script>