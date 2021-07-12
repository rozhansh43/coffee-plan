<template>
  <div class="add-item">
    <form @submit.prevent="emitAdd">
      {{ newitem }}
      <input v-model="newitem" @keyup.enter="increaseitem">

      <button type="submit">
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
  props: ['items'],
  data() {
    return {
      // parentData: this.$parent.items,
      newitem: ""

    }
  },
  methods: {
     emitAdd () {
       this.$emit('increase', this.newitem)
       this.newitem= "";
    },
  }
}
</script>