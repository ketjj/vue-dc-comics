<template>
  <div>
    <MyHeader/>
    <MyMain />


  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader';
import MyMain from '@/components/MyMain';



export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain

  }
}
</script>

<style lang="scss">
@import './assets/style/vars';
@import './assets/style/general';
@import './assets/style/utilities';
@import './assets/style/mixin';

</style>
