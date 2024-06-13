
<template>
  <div>
  <AccItem
    v-for="(item, index) in items"
    :header="item.header"
    :content="item.content"
    :show="shows[index]"
    @clicked="onClicked(index)"
  />
  </div>

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
      for(let i = 0; i < this.shows.length; i++) {
        this.shows[i] = index === i ? !this.shows[i] : false
      }
    }
  },
  components: { AccItem }
}


</script>