<template>
  <div class="items">
    <ul>
      <li v-for="item in items" :key="item.id" class="item">
        {{ item.name }}

        <button @click="like(item)">
          Like ({{ item.likeCount }})
        </button> 

        <button @click="remove(item.id)">
          Remove
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    items: { type: Array, default: () => [] }
  },
  methods: {
    like (item) {
      item.likeCount = item.likeCount + 1
    },
    remove (itemId) {
      if (confirm('Are you sure?'))
        this.$emit('remove', itemId)
    }
  }
}
</script>
