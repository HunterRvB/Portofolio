<script setup lang="ts">
</script>

<template>
    <div class="hero-section">
        <h1 class="hero-title">Robin van Barneveld  </h1>
        <h1 class="hero-jobtitle">Front end Developer <br> UX/UI designer</h1>
        <div class="img-wrapper">
            <img src="../assets/profile pic.png" alt="profile Image">
        </div>
    </div>
</template>



<style scoped>

/* Mobile layout (default) */
@media screen and (max-width: 1024px) {
    .hero-section {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        padding: 4rem 1rem;
    
    }
    .hero-title {
        font-size: 2.5rem;
        margin-bottom: 1rem;
    }
    .hero-jobtitle {
        margin: 0.5rem 0 0;
    }
    .img-wrapper {
        margin-top: 2rem;
    }
    img {
        width: 80vw;
    }
}

/* Desktop/grid layout */
@media screen and (min-width: 1024px) {
    .hero-section {
        display: grid;
        grid-template-columns: 1fr 1fr;
        align-items: flex-start;
        padding: 4rem 2rem;
        
    }

    .hero-title {
        grid-column: 1;
        grid-row: 1 ;
        font-size: 3rem;  
      }
    .hero-jobtitle {
        grid-column: 1;
        grid-row: 2;
        margin: 0;
        font-size: 2.25rem;
    }

    .img-wrapper {
        grid-column: 2 / span 2;
        grid-row: 1 / span 2;
        justify-self: center;
        align-self: center;
        width: 100%;
        max-width: 520px;
    }
    .img-wrapper img {
        display: block;
        width: 100%;
        height: auto;
        border-radius: 8px;
        object-fit: cover;
    }
}

</style>