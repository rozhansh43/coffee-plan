<template>
  <div>
    <div class="content">
      <h1 class="title">
        Coffee plans
      </h1>

      <h2 class="subtitle">
        we travel the world
      </h2>

      <add-item @add="add" />

      <items :items="items" @remove="remove"/>
    </div>
  </div>
</template>

<script>
import Items from '@/components/Items'
import AddItem from '@/components/AddItem'

export default {
  name: 'Home',
  components: {
    Items,
    AddItem
  },
  data () {
    return { 
      items: []
    }
  },
  methods: {
    add (name) {
      this.items.push({
        id: String(Math.floor(Math.random() * 999999999)),
        name,
        likeCount: 0
      })
    },
    remove (itemId) {
      this.items = this.items.filter(o => o.id !== itemId)
    }
  }
}
</script>

