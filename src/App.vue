<template>
  <div id="app">
    <!-- header area -->
    <topBar></topBar>
    <searchBar></searchBar>
    <navbar @activeTabName = "updateTabName"></navbar>
    
  <!-- content -->        
    <div class ="grey"  ref="homeDiv" v-if="this.activeTabName == 'home' | this.activeTabName == null">
        <home></home>
    </div>
    <div class ="grey" ref="aboutDiv" v-else-if="this.activeTabName == 'about'">
        <aboutUS></aboutUS>
    </div>
    <div class ="grey" ref="newProdDiv" v-else-if="this.activeTabName == 'new'">
        <newProducts></newProducts>
    </div>
    <div class ="grey" ref="contactDiv" v-else-if="this.activeTabName == 'contact'">
        <contactUs></contactUs>
    </div>
    <div class ="grey" ref="blogDiv" v-else-if="this.activeTabName == 'blog'">
        <blog></blog>
    </div>
    <div class ="grey" v-else-if="this.activeTabName == 'delivery'" > <!-- delivery comes from the linksBar.vue in the footer -->
        <delivery></delivery>
    </div>
    <div class ="grey" v-else-if="this.activeTabName == 'secure'" > <!-- secure comes from the linksBar.vue in the footer -->
        <securePayment></securePayment>
    </div>
    <div class ="grey" v-else-if="this.activeTabName == 'exchange'" > <!-- exchange comes from the iconsBar.vue in the footer -->
        <exchangePolicy></exchangePolicy>
    </div>
     <div class ="grey" v-else-if="this.activeTabName == 'cash'" > <!-- exchange comes from the iconsBar.vue in the footer -->
        <cashOnDelivery></cashOnDelivery>
    </div>
     <div class ="grey" v-else-if="this.activeTabName == 'shipping'" > <!-- exchange comes from the iconsBar.vue in the footer -->
        <freeShipping></freeShipping>
    </div>
     <div class ="grey" v-else-if="this.activeTabName == 'gift'" > <!-- exchange comes from the iconsBar.vue in the footer -->
        <giftOffers></giftOffers>
    </div>
     <div class ="grey" v-else-if="this.activeTabName == 'quality'" > <!-- exchange comes from the iconsBar.vue in the footer -->
        <qualityCheckedProducts></qualityCheckedProducts>
    </div>

    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome maha"/> -->

    <!-- footer area  -->
    <iconsBar @iconName= "updateTabName"></iconsBar><hr>
    <linksBar @contentName= "updateTabName" class='linksBar'></linksBar>   
    <copyRight></copyRight>   
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
// import HelloWorld from './components/HelloWorld.vue'
import topBar from './components/header/topBar.vue'
import searchBar from './components/header/searchBar.vue'
import navbar from './components/header/navbar.vue'
import home from './components/home.vue'
import aboutUS from './components/aboutUS.vue'
import newProducts from './components/newProducts.vue'
import contactUs from './components/contactUs.vue'
import blog from './components/blog.vue'
import linksBar from './components/footer/linksBar.vue'
import iconsBar from './components/footer/iconsBar.vue'
import copyRight from './components/footer/copyRight.vue'
import delivery from './components/delivery.vue'
import securePayment from './components/securePayment.vue'
import exchangePolicy from './components/exchangePolicy.vue'
import qualityCheckedProducts from './components/qualityCheckedProducts.vue'
import cashOnDelivery from './components/cashOnDelivery.vue'
import freeShipping from './components/freeShipping.vue'
import giftOffers from './components/giftOffers.vue'

export default {
  name: 'app',
  components: {
       topBar, searchBar,navbar ,home , aboutUS,newProducts,contactUs , blog, linksBar,iconsBar , copyRight,delivery,securePayment,giftOffers,freeShipping,exchangePolicy,cashOnDelivery,qualityCheckedProducts
  },
  data() {
    return{

    }
  },
  props:['activeTabName','contentName','iconName'],
  methods : {
    updateTabName : function(variable) {
      this.activeTabName= variable;
      console.log('this.activeTabName ',this.activeTabName);
    },
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
 
}
.linksBar{
  position: relative;
  bottom: 0px;
}
.grey{
  background-color: #F0F2F5;
}
</style>
