<template>
    <b-container>
        
        <b-row>
            <b-col cols="4"> 
                <h2><strong><a class="nav-link brand" href="#"><span class="yellow">CACTUS</span> SHOP</a></strong></h2>
                 <h6 class="brand-comment">The best online shopping platform</h6>
            </b-col>
            <b-col cols="5"><br><br>
                <!-- <input type="text" class="form-control" placeholder="Search our catalog .." aria-label="Username" aria-describedby="basic-addon1"> -->
                <b-form-input id="input-small" size="sm" placeholder="Search our catalog ..."></b-form-input>
            </b-col>
            <b-col offset-md="1"><br>
                <b-dropdown text="Acount" variant="outline" class="m-2">
                    <b-dropdown-item href="#">Login</b-dropdown-item>
                    <b-dropdown-item href="#">Register</b-dropdown-item>
                </b-dropdown>
            </b-col>
        </b-row>

    </b-container>
    
</template>

<script>
export default {
  name: 'searchBar',
}
</script>

<style scoped>

html, body {
    background-color: #fff;
    font-family: 'Nunito', sans-serif;
    margin:0 auto;
    padding:0;
}
.flex-center {
    align-items: center;
    display: flex;
    justify-content: center;
}

.position-ref {
    position: relative;
}

.top-right {
    position: absolute;
    right: 10px;
    top: 18px;
}

.content {
    text-align: center;
}

.title {
    font-size: 84px;
}

.links > a {
    color: #636b6f;
    padding: 0 25px;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: .1rem;
    text-decoration: none;
    text-transform: uppercase;
}

.m-b-md {
    margin-bottom: 30px;
}
.row{
    width:100%;
}
.borderBox{
    border-radius:0px;
}
.footerBox{
    position: relative;
    bottom:-7px;
}
.blue{
    background-color: #0984e3 ;
    color:white;
}
.headMenu{
    float: right;
}
.yellow{
    color:#fdcb6e;
}
.light-green{
    color:#55efc4;
}
.bg-light-green{
    background-color: #55efc4;
}
.categ-nav{
    width:100%;
    height:100%;
    margin:-8px;
    letter-spacing:2px;
}
.dropdown-toggle:after{
    float:right;
    margin-top:8px;
}
.brand{
    letter-spacing: 2px;
}
.brand-comment{
    padding:0 0 10px 15px;
    color:#2d3436;
    font-size: 1.1em;
}
.cart{
    width:100%;
    height:100%;
}
.fa-shopping-cart{
    font-size: 24px;
    padding-right: 8px;
    /*padding-right:33px;*/
}
.yellow-background{
    background-color:#fdcb6e;
}
.cart-products-count{
    font-size: 1.2em;
}
.currency-div{
    position:absolute;
    right:5%
}
.input-group-append{
    height: 39%;
}

/*extra Small devices (landscape phones, 576px and up)*/
@media (max-width: 575.98px){
    .hot-sale-div{
        display: none;
    }
    .logo-div{
        text-align: center;
    }
    .user-account{
        color:white;
        position:relative;
        right:85%;
        padding-bottom:5px;
    }
    .searchdiv{
        display: none;
    }
}

/* Small devices (landscape phones, 576px and up)*/
@media (min-width: 576px) and (max-width: 767.98px){
    .hot-sale-div{
        display: none;
    }
    .logo-div{
        text-align: center;
    }
    .searchdiv{
         display: none;
     }
}

/* Medium devices (tablets, 768px and up)*/
@media (min-width: 768px) and (max-width: 991.98px){
    .hot-sale-div{
        display: none;
    }
    .logo-div{
        text-align: center;
    }
    .search-dest{
        display:none;
    }
}

/* Large devices (desktops, 992px and up)*/
@media (min-width: 992px) and (max-width: 1199.98px){
    .lang-div{
        position:absolute;
        right:12%
    }
    .search-dest{
        display:none;
    }
}

/* Extra large devices (large desktops, 1200px and up)*/
@media (min-width: 1200px) {
    .lang-div{
        position:absolute;
        right:12%
    }
    .search-dest{
        display:none;
    }
}
</style>
