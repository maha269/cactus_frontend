<template>
        <div class="container">
            <br><br>
            <b-row>
                <b-col>
                    <h5>Information</h5>
                    <ul>
                        <li v-for='link in links'>
                            <a class="contentLink"  @click="updateTabName(link.name)">{{link.description}}</a>
                        </li>
                    </ul>
                </b-col>
                <b-col>
                    <h5>Useful Links</h5>
                    <ul>
                        <li v-for='link in links'>
                            <a class="contentLink"  @click="updateTabName(link.name)">{{link.description}}</a>
                        </li>
                    </ul>
                </b-col>
                <b-col>
                    <h5>Contact Us</h5>
                    <p>
                        building 20, Zayed city, Giza governorate, ARE .
                    </p>
                    <p>
                        +2 010 1108 8902
                    </p> 
                    <p>
                        test@test.com
                    </p><br>
                    <ul class="social">
                        <li> <a target="_blank" href="https://www.facebook.com/Cactus-shop-346268902739863/"><i class="fab fa-facebook-square fa-2x facebook" aria-hidden="true"></i></a> </li>
                        <li> <a target="_blank" href="https://www.twitter.com/"><i class="fab fa-twitter fa-2x twitter"></i></a> </li>
                        <li> <a target="_blank" href="https://www.instagram.com/"><i class="fab fa-instagram fa-2x instagram"></i></a> </li>
                        <li> <a target="_blank" href="https://www.youtube.com/"><i class="fab fa-youtube fa-2x youtube"></i></a> </li>
                    </ul>
                </b-col>
                <b-col>
                    <h5>Newsletter</h5>
                    <p>Get our latest news and special sales</p>
                    <input class="form-control" type="text" placeholder="Your Email Address"><br>
                    <p>You may unsubscribe at any moment. For that purpose, please find our contact info in the legal notice.</p>
                </b-col>
            </b-row>
        </div>
</template>

<script>

export default {
  name: 'linksBar',
  data(){
      return{
          links:[
              {
                  name:'delivery',
                  description:'Delivery'
              },
               {
                  name:'about',
                 description:'About Us'
              },
                {
                  name:'secure',
                  description:'Secure payment'
              },
              {
                  name:'contact',
                 description:'Contact US'
              },
              

          ],
          usefulLinks:[
               {
                  name:'delivery',
                  description:'Delivery'
              },
               {
                  name:'about',
                 description:'About Us'
              },
                {
                  name:'secure',
                  description:'Secure payment'
              },
              {
                  name:'contact',
                 description:'Contact US'
              },
          ],
          contentName:null ,
      }
  }, methods : {
          updateTabName(name){
              this.contentName = name;
              this.$emit("contentName" , this.contentName);
          }
  },
}
</script>
<style scoped>

ul{
    list-style: none;
    padding-left: 0px;
}
.social{
    display:inline-block ;
}
.social li{
    float:left ;
    margin :5px;
}
.facebook{
    color:#4E71A8;
}
.twitter{
    color:#1CB7EB;
}
.youtube{
    color:#CA3737;
}
.instagram{
    color:#3B3839;
}
li , p{
    color:#9EA1A2;
}
li:hover{
    color:#374E68;
}
.center{
    text-align: center;
}
.contentLink{
    cursor: pointer;
}

</style>
