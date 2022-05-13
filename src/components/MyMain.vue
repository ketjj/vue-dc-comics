<template>
  <main>
    <div class="k_container">
      <h2> --> CONTENT GOES HERE -- </h2>
    </div>
  </main>
  
</template>

<script>
export default {
  name: 'MyMain'

}
</script>

<style lang="scss">
@import '../assets/style/mixin';
@import '../assets/style/vars';

main{
  min-height: 120px;
  background-color: black;
  color: white;
   .k_container{
    height: 120px;
    display: flex;
    align-items: center;
   }   
}
</style>