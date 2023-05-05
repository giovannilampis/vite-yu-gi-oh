<script >

import headerComp from './components/HeaderComp.vue'

export default{
  name: 'app',
  components: {
    headerComp
  }
}

</script>

<template>
  <headerComp/>
</template>

<style lang="scss">
@use './style/main.scss';
</style>
