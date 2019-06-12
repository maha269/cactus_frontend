<template>
        <div class="container">
            <br><br>
            <b-row>
                 <b-col class="center icon-col"  v-for="link in links" @click="updateTabName(link.name)">
                    <div class="icon" v-html="link.icon"></div><br><br>
                    <p>{{link.after}}</p>
                </b-col>
            </b-row>
        </div>
</template>

<script>
export default {
  name: 'iconsBar',
  data(){
      return{
          links:[
              {
                  name:'exchange',
                  href:'#',
                  icon:'<i class="fa fa-reply"></i>',
                  after:'3 days exchange policy'
              },
               {
                  name:'shipping',
                  href:'#',
                  icon:'<i class="fa fa-plane"></i>',
                  after:'free shipping all over the world'
              },
                {
                  name:'cash',
                  href:'#',
                  icon:'$$',
                  after:'Cash on Dlivery'
              },
              {
                  name:'quality',
                  href:'#',
                  icon:'<i class="fa fa-star"></i>',
                  after:'Quality checked products'
              },
              {
                  name:'secure',
                  href:'#',
                  icon:'<i class="fa fa-lock"></i>',
                  after:'Secure payment system'
              },
              {
                  name:'gift',
                  href:'#',
                  icon:'<i class="fa fa-gift"></i>',
                  after:'Limited special gift offers'
              },

          ],
          iconName:null,
      }
  },methods:{
      updateTabName(name){
              this.iconName = name;
              this.$emit("iconName" , this.iconName);
          }
  }
}
</script>

<style scoped>

.icon {
  display: inline-block;
  /* width: 35px; */
  margin:0 auto;
  border-radius: 60px;
  box-shadow: 0px 0px 7px #0984E3;
  padding: 0.5em 0.6em;
    text-align: center;
    color:#0984E3;

}
.fa{
    color:#0984E3;
    background-color:#0984E3;

}
.center{
    text-align: center;
}
.icon-col{
    cursor:pointer;
}
</style>
