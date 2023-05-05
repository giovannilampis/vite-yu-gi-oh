<script >

import headerComp from '../src/assets/components/HeaderComp.vue'

export default{
  name: 'app',
  components: {
    headerComp
  }
}

</script>

<template>
  <headerCom :titleProps=" 'Yu-Gi-Oh Api' "/>
</template>

<style lang="scss">
@use './style/main.scss';
</style>
