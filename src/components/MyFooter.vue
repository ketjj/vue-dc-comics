<template>
  <footer>
    
      <div class="upper">
        <div class="k_container">
          <div class="left d-flex">

            <div class="row row-cols-1"> 
              <!-- FIRST COL -->
              <div class="col">
                <h6>dc comics</h6>
                <ul>
                  <li><a href="#">Characters</a></li>
                  <li><a href="#">Comics</a></li>
                  <li><a href="#">Movies</a></li>
                  <li><a href="#">TV</a></li>
                  <li><a href="#">Games</a></li>
                  <li><a href="#">Videos</a></li>
                  <li><a href="#">News</a></li>
                </ul>

                <h6>shop</h6>
                <ul>
                  <li><a href="#">Shop DC</a></li>
                  <li><a href="#">Shop DC Collection</a></li>
                </ul>
              </div>
              <div class="col">
                <h6>dc</h6>
                <ul>
                  <li><a href="#">Terms of Use</a></li>
                  <li><a href="#">Privacy Policy(New)</a></li>
                  <li><a href="#">Ad choices</a></li>
                  <li><a href="#">Advertising</a></li>
                  <li><a href="#">Jobs</a></li>
                  <li><a href="#">Subscription</a></li>
                  <li><a href="#">Talent Workshops</a></li>
                  <li><a href="#">CPSC Certificates</a></li>
                  <li><a href="#">Ratings</a></li>
                  <li><a href="#">Shop Help</a></li>
                  <li><a href="#">Contact Us</a></li>
                </ul>
              </div>
              <div class="col">
                <h6>sites</h6>
                <ul>
                  <li><a href="#">DC</a></li>
                  <li><a href="#">MAD Magazines</a></li>
                  <li><a href="#">DC Kids</a></li>
                  <li><a href="#">DC Universe</a></li>
                  <li><a href="#">DC Power Visa</a></li>
                </ul>
              </div>
            </div>

            
          <div class="image d-flex align-items-center">
            <img src="../assets/img/dc-logo-bg.png" alt="">
          </div>
          </div>
        </div>
      </div>

      <div class="lower">
        <div class="k_container">
          <div class="button">
            sing-up now!
          </div>

          <div class="icons d-flex">
            <div>follow us</div>
            <div v-for="(icon,index) in iconsList" :key="`icon-${index}`" class="list-icons">
              <i :class="icon"></i>
              <!-- <i class="{{icon}}"></i> -->
            </div>
          </div>
        </div>
      </div>

  </footer>
</template>

<script>
export default {
  name: 'MyFooter',

  data(){
    return{
      iconsList: [
        'fa-brands fa-facebook-f',
        'fa-brands fa-twitter',
        'fa-brands fa-youtube',
        'fa-brands fa-pinterest-p',
        'fa-solid fa-location-dot'
      ],


      firstColumn: [
        {
          title: 'dc comics',
          list: [
            'Characters',
            'Comics',
            'Movies',
            'TV',
            'Games',
            'Videos',
            'News'
          ]          
        },
        {
          title: 'shop',
          list: [
            'Shop DC',
            'Shop DC Collectibles',
            ]
        }
      ]
    }
  }


}
</script>

<style lang="scss">
@import '../assets/style/mixin';
@import '../assets/style/vars';

footer{
  color: $color-white;
  .upper{
    height: 350px;
    background-image: url(../assets/img/footer-bg.jpg);
    overflow: hidden;
    @include imageCenter;
    .col{
      padding-left: 0;
      height: 200px;
    }
    img {
      height: 450px; 
    }
    li a{
      font-size: 12px;
      line-height: .5;
      color: lighten($secondary-color, 40% );
      &:hover{
        color: lighten($secondary-color, 70% );
        cursor: pointer;
      }  
    }
    h6{
      font-weight: 600;
      @include upper;
    }
    .row{
      width: 40%;
      margin: 40px 0;
    }
    .left{
      justify-content: space-between;
      height: 100%;
    }
  }
  .lower{
    height: 70px;
    background-color: lighten($secondary-color, 10%);
    .k_container{
      @include spaceBetween;
      .button{
        font-size: 14px;
        @include upper;
        padding: 8px 16px;
        border: 2px solid $primary-color;
        &:hover{
          background-color: lighten($primary-color, 20%);
          @include pointer;
          transition: .4s all;
          color: black;
        }
      }
      }
      .icons{
        @include center;
        div{
         color: lighten($primary-color, 20%);
         @include upper;
         font-weight: 600;
         margin-right: 15px;

        }
        .list-icons{
          @include center;
          width: 30px;
          height: 30px;
          background-color: lighten($secondary-color, 30%);
          border-radius: 50%;
          margin-right: 12px;
          &:hover{
            background-color: lighten($secondary-color, 50%);
            @include pointer;
          }
        }
        i {
          font-size: 14px;
          color: lighten($secondary-color, 10%);         
        }
      }

    }
  }


</style>