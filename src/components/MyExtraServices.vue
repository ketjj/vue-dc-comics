<template>

 <div class="extraa">
    <div class="k_container">
     <div v-for="(service, index) in services" :key="`icons-${index}`">
       <img :src="require(`../assets/img/${service.iconUrl}${service.formatImage}`)" :alt="`${service.title}`" width:20px > 
       <!-- <img src="../assets/img/buy-comics-digital-comics.png" alt="digital comics"> -->
       <span>{{service.title}}</span>
     </div>
    </div>
 </div>
  
</template>

<script>
export default {
  name:'MyExtraServices',

  data(){
    return {
      services: [
        {
          href: '#',
          iconUrl:  'buy-comics-digital-comics',
          formatImage: '.png',
          title: 'digital comics',
        },
        {
          href: '#',
          iconUrl:  'buy-comics-merchandise',
          formatImage: '.png',
          title: 'dc merchandise'
        },       
        {
          href: '#',
          iconUrl:  'buy-comics-subscriptions',
          formatImage: '.png',
          title: 'subscription'
        },  
        {
          href: '#',
          iconUrl:  'buy-comics-shop-locator',
          formatImage: '.png',
          title: 'comic shop location'
        },  
        {
          href: '#',
          iconUrl:  'buy-dc-power-visa',
          formatImage: '.svg',
          title: 'dc power visa'
        },  
      ]
    }  
    
  }
}
</script>

<style lang="scss">
@import '../assets/style/mixin';
@import '../assets/style/vars';

.extraa{
  background-color: $primary-color;
  height: 140px;
  color: $color-white;
  .k_container{
    @include center;
    padding: 0 0 0 40px;
    div{
    flex-basis: calc(100% / 5);
    display: flex;
    align-items: center ;
    margin-right: 20px;
    span{
      margin-left: 10px;
      font-size: 12px;
      @include upper;
    }
    }
    img{
      max-width: 42px;
      height: 50px;
    }

  }
}

</style>