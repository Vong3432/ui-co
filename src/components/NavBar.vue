<template>
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
</template>

<script>
export default {
    
}
</script>

<style scoped>

</style>


