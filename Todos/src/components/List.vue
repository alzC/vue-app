<style src="./List.css"></style>

<template>
 <Flipper :flipKey="active">
  <ul class="list">
    <li v-for="item in items" :key="item" @click="onClick(item)">
      <ListItem item="item" :expanded="active === item"/>
    </li>
  </ul>
  </Flipper>
</template>

<script>
import ListItem from './ListItem'
import { Flipper } from 'vue-flip-toolkit'




export default {
  components: {ListItem, Flipper},
  data () {
    return {
      items: [1, 2, 3, 4, 5],
      active: 0 
      
    }
  },
  methods: {
    onClick (item) {
      this.active = this.active === item ? 0 : item
    }
    
  }
}
</script>
