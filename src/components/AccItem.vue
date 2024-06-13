<template>
<div>
  <div class="header" @click="onClick">{{ header }}</div>
  <div class="content" v-if="show">{{ content }}</div>
</div>

</template>

<script>

export default {
  name: 'AccItem',
  props: {
    header: String,
    content: String,
    show: Boolean
  },
  methods: {
    onClick () {
      this.$emit('clicked')
    }
  }
}

</script>