<template>
  <div>
    <MyHeader/>
    <MyMain />
    <MyExtraServices/>
    <MyFooter />


  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader';
import MyMain from '@/components/MyMain';
import MyExtraServices from '@/components/MyExtraServices';
import MyFooter from '@/components/MyFooter';


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyExtraServices,
    MyFooter

  }
}
</script>

<style lang="scss">
@import './assets/style/vars';
@import './assets/style/general';
@import './assets/style/utilities';
@import './assets/style/mixin';

</style>
