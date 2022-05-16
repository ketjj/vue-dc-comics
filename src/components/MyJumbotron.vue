<template>
  <div class="Jumbo">

  </div>
  
</template>

<script>
export default {
  name:'MyJumbotron'

}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixin';
@import '../assets/style/vars';

.Jumbo{
  width: 100%;
  background-image: url('../assets/img/jumbotron.jpg');
  // @include imageCenter;
  background-position: top;
  background-size: cover;
  height: 350px;
}



</style>