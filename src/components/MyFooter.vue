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
                  <li>Characters</li>
                  <li>Comics</li>
                  <li>Movies</li>
                  <li>TV</li>
                  <li>Games</li>
                  <li>Videos</li>
                  <li>News</li>
                </ul>

                <h6>shop</h6>
                <ul>
                  <li>Shop DC</li>
                  <li>Shop DC Collection</li>
                </ul>
              </div>
              <div class="col">
                <h6>dc</h6>
                <ul>
                  <li>Terms of Use</li>
                  <li>Privacy Policy(New)</li>
                  <li>Ad choices</li>
                  <li>Advertising</li>
                  <li>Jobs</li>
                  <li>Subscription</li>
                  <li>Talent Workshops</li>
                  <li>CPSC Certificates</li>
                  <li>Ratings</li>
                  <li>Shop Help</li>
                  <li>Contact Us</li>
                </ul>
              </div>
              <div class="col">
                <h6>sites</h6>
                <ul>
                  <li>DC</li>
                  <li>MAD Magazines</li>
                  <li>DC Kids</li>
                  <li>DC Universe</li>
                  <li>DC Power Visa</li>
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
        <div class="k_container">BBBB
        </div>
      </div>

  </footer>
</template>

<script>
export default {
  name: 'MyFooter'

}
</script>

<style lang="scss">
@import '../assets/style/mixin';
@import '../assets/style/vars';

footer{
  .upper{
    height: 350px;
    background-image: url(../assets/img/footer-bg.jpg);
    overflow: hidden;
    color: white;
    @include imageCenter;
    .col{
      padding-left: 0;
    }
    img {
      height: 450px; 
    }
    li {
      font-size: 12px;
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

  }
}

</style>