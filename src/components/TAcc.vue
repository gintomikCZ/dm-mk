
<template>
  <AccItem
    v-for="(item, index) in items"
    :header="item.header"
    :content="item.content"
    :show="shows[index]"
    @clicked="onClicked(index)"
  />
</template>



<script>

import AccItem from '@/components/AccItem.vue'

export default {
  name: 'TAcc',
  props: {
    items: Array
  },
  data() {
    return {
      shows: []
    }
  },
  created () {
    for(let i = 0; i < this.items.length; i++) {
      this.shows.push(false)
    }
  },
  methods: {
    onClicked (index) {
      console.log(this.shows)
      for(let i = 0; i < this.items.length; i++) {
        if (index === i) {
          console.log('shoda', i)
          this.shows[i] = !this.shows[i]
        } else {
          console.log('neshoda', i)
          this.shows[i] = false
        }
      }
      console.log(this.shows)
    }
  },
  components: { AccItem }
}


</script>