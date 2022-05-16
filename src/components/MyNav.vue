<template>
     <nav class="nav_bar">
      <ul class="nav_list">
        <li v-for="(list, index) in menuList" :key="`menu-${index}`"
        :class="{'active': list.isActive}">
          <a href="#">{{list.category}}</a>
        </li>    
      </ul>
    </nav>
</template>

<script>
export default {
  name: "MyNav",
  props: {
    menuList: Array,
  }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixin';
@import '../assets/style/vars';

nav{
      line-height: 55px;
      }
      .nav_bar,
      .nav_list{
        height: 100%;
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

</style>