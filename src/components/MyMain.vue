<template>
  <main>
    <div class="k_container py-5">
      <MyMainCards
      v-for="(card, index) in DCcomics" :key="index"
      class="k_card"
      :card="card"
       />

    </div>

  </main>
  
</template>

<script>
import DCcomics from '../assets/data/DCcomics'
import MyMainCards from '@/components/MyMainCards'
export default {
  name: 'MyMain',
  components: {MyMainCards },
  data(){
    return{
      DCcomics
    }
  }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixin';
@import '../assets/style/vars';

main{
  background-color: $secondary-color;
  color: $color-white;
   .k_container{
    min-height: 120px;
    display: flex;
    justify-content: start;
    flex-wrap: wrap;
    align-items: center;
   }
  
}
</style>