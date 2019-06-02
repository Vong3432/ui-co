<template>

    <section :class="[ this.types === 'hero' ? 'hero-section': 'content-section']">
        <b-container>
            <slot></slot>
        </b-container>
    </section>    

</template>

<script>

export default {
    props:{
        types:{
            type:String,
            required:true
        }
    },
    data() {
        return {
            
        }
    },

    
}
</script>

<style scoped>

.hero-section::before
{
    content: '';
    background-image: url(../images/hero-bg.jpg);
    background-size: cover;
    background-position:center;
    position: absolute;
    width: 100%;
    z-index: -1;
    background-color: #141414;
    background-blend-mode: overlay;
    min-height: inherit;
    height: 100%;
}

.hero-section,.content-section
{   
    position:relative;    
    width:100%;
    min-height:60vh;
    
    display:flex;
    flex-flow:column;
    align-items: center;
    justify-content: center;
}

.hero-section h2
{
    color:#fff;
}

.new-product-section
{
    background: #FBFBFB;        
    padding-bottom: 5em;    
}

.default-product-section
{
    padding-bottom:5em;
}

.new-product-container
{    
    display: flex;
    flex-flow: row wrap;
    width:100%;
    min-height: inherit;        
}

.default-product-container
{            
    display: grid;
    grid-gap: 20px;
    grid-template-areas: "c c c c"
                         "c c c c";
    width:100%;
    grid-auto-columns: minmax(auto,300px);
    min-height: inherit;        
}

.new-product-container img
{
    width:inherit;
    height: 250px;
    object-fit: cover;
}

.new-product-container .main--info
{
    display:flex;
    flex-flow: row;    
    border-bottom: 5px solid #141414;
    padding: 0;
}

@media screen and (max-width: 750px)
{
    .default-product-container
    {
        grid-template-areas: "c c"
                             "c c";
        grid-auto-columns: 1fr;  
              
    }
}
</style>


