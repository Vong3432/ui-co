<template>
  <div id="app">
    <b-navbar toggleable="lg" class="navbar">

      <b-container>
        <b-navbar-brand href="#">UI.Co</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>     
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">            

            <b-nav-item href="#" class="mr-md-3">Home</b-nav-item>
            <b-nav-item href="#" class="mr-md-3">About us</b-nav-item>
            <b-nav-item-dropdown text="Products" right>
              <b-dropdown-item href="#">Product A</b-dropdown-item>
              <b-dropdown-item href="#">Product B</b-dropdown-item>
              <b-dropdown-item href="#">Product C</b-dropdown-item>             
            </b-nav-item-dropdown>
            
          </b-navbar-nav>
        </b-collapse>

      </b-container>

  </b-navbar>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'


export default {
  name: 'app',
  data() {
      return {
        dismissSecs: 10,
        dismissCountDown: 0,
        showDismissibleAlert: false
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
    
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins&display=swap');

#app {
  font-family: Helvetica, Arial, sans-serif,'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;  
  color: #2c3e50;  
}

.navbar
{
  padding-top: 2em;
  padding-bottom: 2em;
}


</style>
