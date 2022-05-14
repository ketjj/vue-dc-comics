<template>
 <header>
   <div class="k_container">

    <img src="../assets/img/dc-logo.png" alt="">

    <nav class="nav_bar">
      <ul class="nav_list">
        <li v-for="(list, index) in menu" :key="`menu-${index}`"
        :class="{'active': list.isActive}">
          <a href="#">{{list.category}}</a>
        </li>    
      </ul>
    </nav>
   </div>
 </header>
  
</template>

<script>
export default {
  name: 'MyHeader',
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
    nav{
      line-height: 55px;
      }
      .nav_bar,
      .nav_list{
        height: 100%;
      }
      img{
      width: 65px;
      }
      ul{
      display:flex;
      margin-bottom: 0;
      align-items: center;
      }
      .nav_list{
        padding:0;
      }

      ul li {
      height: 100%;
      margin-right: 10px;
      padding: 10px;
      padding-top: 20px;
      font-size: 12px;
      &:hover{
      border-bottom: 4px solid $primary-color;
      cursor: pointer;
      }
      &.active{
        background-color: lighten($primary-color, 40% ) ;
      }
      }
      
      a{
      @include upper;
      color: black;
      }

  }
}


</style>