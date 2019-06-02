<template>

  <div id="app" style="min-height:150vh">

    <NavBar />

    <Hero types="hero">
        <h2 class="text-center">FINDS MORE ON UI.CO</h2>
        <b-input-group class="mt-3">
          <b-input-group-text slot="append"><strong class="text-danger">!</strong></b-input-group-text>
          <b-form-input placeholder="Search product"></b-form-input>
        </b-input-group>
    </Hero>

    <Hero types="content" class="new-product-section">

        <h2 class="text-center" style="padding-top:2em;padding-bottom:2em">WHAT'S NEW ON UI.CO?</h2>

        <div class="new-product-container">         

            <b-media-aside class="col-12 col-sm-4" vertical-align="center">              
              <b-img-lazy src="./images/sampleProduct1.jpg" alt="sample1"></b-img-lazy>
            </b-media-aside>

            <b-media-body class="my-5 my-sm-auto ml-0 ml-sm-3 col-12 col-sm-8">
              
              <div class="main--info col-12 py-3">
                <h5 class="mt-0 header">IPHONE XS</h5>               
                <span class="price-tag mx-3">RM3999.00</span>
              </div>

              <p class="py-3">
                Though the gravity still dragged at him, his muscles were making great efforts to adjust. After the daily classes he no longer collapsed immediately into bed. Only the nightmares got worse.
              </p>  
              <span class="">
                <a href="#" class="primary-link">View details</a>                
              </span>

            </b-media-body>            

        </div>       
        

    </Hero>

    <Hero types="content" class="default-product-section">
      <h2 class="text-left" style="padding-top:2em;padding-bottom:2em">HOT PRODUCTS</h2>
   
          <ProductCard class="default-product-container">
            
            <b-card 
            v-for="item in this.hotProducts" 
            :key="item.id"   
            :img-src="require('./images/'+item.image)"
            img-alt="Card image" 
            img-top
            class=""
            >              
              <b-card-text>                
                <p class="card-name">{{item.name}}</p>
                <small>{{item.categories}}</small>
                <p class="price">{{item.price}}</p>
              </b-card-text>

            </b-card>

          </ProductCard>
     
    </Hero>

  </div>

</template>

<script>
import NavBar from './components/NavBar.vue'
import Hero from './pages/Hero.vue'
import ProductCard from './components/ProductCard.vue'

export default {
  name: 'app',
  data() {
      return {
        dismissSecs: 10,
        dismissCountDown: 0,
        showDismissibleAlert: false,
        hotProducts:[
                {
                    id: 0,
                    image:"sunglasses.jpg",
                    name: "Sunglasses",
                    categories: "Fashion",
                    price: "RM3999.00"
                },
                {
                    id: 1,
                    image:"drone.jpg",
                    name: "Drone",
                    categories: "Fashion",
                    price: "RM3999.00"
                },
                {
                    id: 2,
                    image:"airpod.jpg",
                    name: "Airpod",
                    categories: "Fashion",
                    price: "RM3999.00"
                },
                {
                    id: 3,
                    image:"shampoo.jpg",
                    name: "Shampoo",
                    categories: "Daily",
                    price: "RM99.00"
                },
                {
                    id: 4,
                    image:"bowl.jpg",
                    name: "Bowl",
                    categories: "Daily",
                    price: "RM99.00"
                },
                {
                    id: 5,
                    image:"supreme.jpg",
                    name: "Supreme T-Shirt",
                    categories: "Fashion",
                    price: "RM59.00"
                }
                
        ]
      }
    },
    methods: {
      countDownChanged(dismissCountDown) {
        this.dismissCountDown = dismissCountDown
      },
      showAlert() {
        this.dismissCountDown = this.dismissSecs
      }
  },
  components: {
    NavBar,
    Hero,
    ProductCard
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins&display=swap');

#app {
  font-family: 'Poppins', sans-serif, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;    
}

h1,h2,h3,h4,h5,h6,.navbar-brand,.header
{
  font-family: Arial;
  font-weight: bold;  
}

h1,h2,h3,h4,h5,h6
{
  font-size: 2.5rem;
}

.header
{
  font-size: 1.8rem;
  color: #141414;
}

.price-tag
{
  background: #0EAB3A;
  color: #fff;

  max-width: 150px;
  max-height: 100px;
  width:auto;
  height:100%;

  font-size: .8rem;
  text-align: center;
  letter-spacing: 1.5px;
  font-weight: bold;

  padding:.8em 1em;
}

.primary-link
{
  text-decoration: underline;
}

.navbar
{
  padding-top: 2em;
  padding-bottom: 2em;
}


</style>
