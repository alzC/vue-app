<template>
  <Flipped :flIpId="flipId">
    <div class="listItem" :class="{isExpanded: expanded}">
    <div class="listItemContent">
      <div class="avatar"></div>
      <div class="description">
        <div></div>
        <div></div>
        <div></div>
      </div>
      <div class="additional-content" v-if="expanded">
        <div></div>
        <div></div>
        <div></div>
      </div>
    </div>
  </div>
  </Flipped>
</template>

<script>
  
  import { Flipped} from 'vue-flip-toolkit'

  export default {
    components: { Flipped},

    computed: {
      flipId () {
        return `listItem-${this.item}`
      }
    },
    
    props: {
      item: Number,  
      expanded: Boolean
    }
  }
  
</script>
