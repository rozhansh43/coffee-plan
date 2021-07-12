<template>
  <div class="add-item">
    <form>
      {{ newitem }}
      <input v-model="newitem" @keyup.enter="increaseitem">

      <button @click.prevent="increaseitem" @click="$emit('increase')">
          insert
      </button>

      <!-- <ul>
        <li v-for="item in items" :key="item.id">
        {{ parentData.name }}
        </li>
      </ul> -->
      
    </form>
  </div>
</template>

<script>
export default {
  props: ['newitem'],
  data() {
    return {
      // parentData: this.$parent.items,
    }
  },
  methods: {

  }
}
</script>