<template>
  
     <div class="k_card row row-cols-2 row-cols-sm-3 row-cols-xl-6">

        <div class="col">
          <div>
            <img :src="card.thumb" alt="card.series">
          </div>
          <h5>{{card.series}}</h5>

        </div>
      </div>


</template>

<script>

export default {
  name: "MyMainCards",
  props: {
    card: Object,
  }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixin';
@import '../assets/style/vars';

.k_container{
    min-height: 120px;
    display: flex;
    justify-content: start;
    
    align-items: center;
   .k_card{
     width: 16%;
     height: 180px;
     flex-wrap: wrap;
     margin:1px;
     margin-top: 15px;
     opacity: .7;
      &:hover{
          opacity: 1;
          cursor: pointer;
        }

     .col{
       height: 180px;
       
     }
     .col,
     img{
       width:100%;
       
     }
     .col div{
       height: 150px;
       overflow: hidden;
       margin-bottom: 10px;
     }
     }
       h5{
        font-size: 10px;
        @include upper;       
       
       }
   }


   


</style>