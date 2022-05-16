<template>
 <header>
   <div class="k_container">

    <img src="../assets/img/dc-logo.png" alt="">

    <MyNav :menuList="menu"/>
   </div>
 </header>
  
</template>

<script>
import MyNav from '../components/MyNav'

export default {
  name: 'MyHeader',
  components: {MyNav},
  data(){
    return {
      menu: [
        {
          href: '#',
          category: 'characters',
          isActive: false
        },
        {
          href: '#',
          category: 'comics',
          isActive: true
        },
        {
          href: '#',
          category: 'movies',
          isActive: false
        },
        {
          href: '#',
          category: 'tv',
          isActive: false
        },
        {
          href: '#',
          category: 'games',
          isActive: false
        },
        {
          href: '#',
          category: 'collectibles',
          isActive: false
        },
        {
          href: '#',
          category: 'videos',
          isActive: false
        },
        {
          href: '#',
          category: 'fans',
          isActive: false
        },
        {
          href: '#',
          category: 'news',
          isActive: false
        },
        {
          href: '#',
          category: 'shop',
          isActive: false
        }

      ]
    }
    
    
  }

}
</script>

<style lang="scss">
@import '../assets/style/mixin';
@import '../assets/style/vars';

header{
  height: 90px;

  .k_container{
    height: 100%;
    @include spaceBetween;
      img{
      width: 65px;
      }} 
  }

</style>