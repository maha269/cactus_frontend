<template>
    <div style="background-color:#0984E3 " >
        <b-nav align="left" class="container">
            <b-nav-item-dropdown style="background-color:#55EFC4" id="my-nav-dropdown" text="Cactus Categories" toggle-class="nav-link-custom" right>
                <b-dropdown-item>Clothes</b-dropdown-item>
                <b-dropdown-item>Electronics</b-dropdown-item>
                <b-dropdown-item>Furniture</b-dropdown-item>
                <b-dropdown-item>Food</b-dropdown-item>
                <b-dropdown-divider></b-dropdown-divider>
                <b-dropdown-item>Kids Toys</b-dropdown-item>
                <b-dropdown-item>Kids Food</b-dropdown-item>
                <b-dropdown-item>Kids Tools</b-dropdown-item>
                <!-- <b-dropdown id="dropdown-dropright" class="dropdown-menu" dropright text="Kids" variant="outline">
                    <b-dropdown-item href="#">Toys</b-dropdown-item>
                    <b-dropdown-item href="#">Food</b-dropdown-item>
                    <b-dropdown-item href="#">Tools</b-dropdown-item>
                </b-dropdown> -->
            </b-nav-item-dropdown>   
             <b-nav-item  v-for="(tab,index) in tabs" v-bind:class="[tab.isActive ? 'active' : '']" @click="toggleClass(index)" @click.prevent="setActiveTabName(tab.name)">
                {{ tab.displayName }}
             </b-nav-item>


             <b-nav-item class= "ml-auto" style="background-color:#FDCB6E" right>
                 <a class=" disabled text-white cart " href="#"><i class="fa fa-shopping-cart"></i></a>
                 &nbsp; <span class="cart-products-count" href="#">0</span>
            </b-nav-item>
        </b-nav>
    </div>
</template>



<script>
// import App from '../App'
// import aboutUS from './aboutUS'

export default {
  name: 'navbar',
  data() {
      return{
        url : '#',
        tabs: [
            {
                isActive : false,
                name: 'home',
                displayName: 'Home',
            },
            {
                isActive: false,
                name: 'new',
                displayName: 'New Products',
            },
            {
                isActive: false,
                name: 'about',
                displayName: 'About us',
            },
            {
                isActive: false,
                name: 'blog',
                displayName: 'Blog',
            },
            {
                isActive: false,
                name: 'contact',
                displayName: 'Contact us',
            }
        ],
        activeTabName: null,
        mounted() {
                // The currently active tab, init as the 1st item in the tabs array
                this.activeTabName = this.tabs[0].name;
            
            },
      }
   
  },
   methods: {
    toggleClass: function(index){
       if(!this.tabs[index].isActive){
         this.tabs.forEach(element => {
            element.isActive = false 
         });
         this.tabs[index].isActive = true;
       }
    },
     setActiveTabName(name) {
      this.activeTabName = name;
      this.$emit("activeTabName" , this.activeTabName);

    },
    displayContents(name) {
      return this.activeTabName === name;
    },
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a{
    color:white;
}
a:hover{
    background-color:#2B4784;
}
 .active{
    background-color:#2B4784;
 }
</style>
