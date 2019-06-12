<template>
    <b-nav>
        <div class="container">
            <ul class="navbar-nav" style="">
                <li class="nav-item active">
                    <a class="nav-link text-danger hot-sale-div" href="#"> <b-spinner type="grow" small></b-spinner>Hot sale offers</a>
                </li>

                <li class="nav-item dropdown lang-div">
                    <b-dropdown text="Language" variant="outline" class="m-2">
                        <b-dropdown-item href="#">English</b-dropdown-item>
                        <b-dropdown-item href="#">Arabic</b-dropdown-item>
                    </b-dropdown>
                </li>
                <li class="nav-item dropdown currency-div">
                    <b-dropdown text="Currency" variant="outline" class="m-2">
                        <b-dropdown-item href="#">US Dollar</b-dropdown-item>
                        <b-dropdown-item href="#">EG Pound</b-dropdown-item>
                    </b-dropdown>
                </li>
            </ul>
        </div>
    </b-nav>
</template>

<script>
export default {
  name: 'topBar'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
li {
list-style: none;
}
a{
    text-decoration: none;
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
