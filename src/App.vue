<template>
  <TAcc :items="[{header: 'header1', content: 'content1'}, {header: 'header2', content: 'content2'}]"/>
</template>


<script>
import TAcc from '@/components/TAcc.vue'
export default {
  name: 'App',
  components: { TAcc }
}


</script>
