<template>    
    <span class="product-card">
        <slot></slot> 
    </span> 
</template>

<script>
export default {
    
}
</script>


<style scoped>


.product-card .card
{
    padding:0;    
    /* max-width: 300px; */
    box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.15);
    border: none;
}

.product-card img
{        
    max-height: 200px;
    object-fit: cover;    
    height:100%;
}

.card-name
{
    font-size: 1.1rem;
    color:#141414;
    font-weight: bold;
}

.price
{
    color: #0EAB3A;
    font-weight: bold;
}

</style>
