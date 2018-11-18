<template>
  <div id="app">
    <!--<v-layout></v-layout> -->
    <!--<v-container></v-container> -->
    <!--<v-radio></v-radio>-->
    <!--<v-is></v-is>-->
    <v-table></v-table>
  </div>
</template>

<script>
import layout from '@/components/layout.vue'
import container from '@/components/container'
import radio from '@/components/radio'
import is from '@/components/inputAndselect'
import table from '@/components/table'
export default {
  name: 'App',
  components: {
    "v-layout" : layout,
    "v-container" : container,
    "v-radio" : radio,
    "v-is" : is,
    "v-table" : table
  }
}
</script>

<style>
</style>
