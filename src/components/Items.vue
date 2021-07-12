<template>
  <div class="items">
    <ul class="ite">
      <li 
      v-for="item in items" 
      :key="item.id"
      class="item"
      >
        {{ item.name }}

        <like-button/>

        <remove-item @remove="removeItem(index)" />
      </li>
    </ul>
  </div>
</template>

<script>
import LikeButton from '@/components/LikeButton'
import RemoveItem from '@/components/RemoveItem'

export default {
  components: {
    LikeButton,
    RemoveItem,
  },
  props: ['items'],
    data () {
    return {
      newitem: ""
    }
  },
  methods: {
    removeItem (index) {
      this.items.splice(index, 1)
    },
  }
}
</script>
