<template>
  <div class="remove-item">
    <button @click="$emit('remove')">
      delete
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
    }
  },
}
</script>