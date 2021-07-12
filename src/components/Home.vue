<template>
  <div>
    <div class="content">
      <h1 class="title">
          Coffee plans
      </h1>

      <h2 class="subtitle">
          we travel the world
      </h2>

      <add-item :newitem="newitem" :items="items"/>
      {{ newitem }}
      <items :items="items"/>
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
      items: [
        { name:'The Addict' , id:0}, 
        { name:'The Curious' , id:1},
        { name: 'The Hacker' , id:2} 
      ],
    }
  },
}
</script>

