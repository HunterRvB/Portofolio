<script setup lang="ts">
</script>

<template>
    <div class="about-section">
        <h1 class="About-title">About me</h1>
        <p class="about-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
             ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
             ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
             ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea </p>
        <div class="icon-wrapper">
            <a href="https://reactjs.org/" target="_blank" rel="noopener noreferrer"><img src="@/assets/icons/react.svg" width="36" height="36" alt="React Icon" class="icon"/></a>
            <a href="https://nextjs.org/" target="_blank" rel="noopener noreferrer"><img src="@/assets/icons/nextjs.svg" width="36" height="36" alt="Next.js Icon" class="icon"/></a>            
            <a href="https://www.figma.com/" target="_blank" rel="noopener noreferrer"><img src="@/assets/icons/figma.svg" width="36" height="36" alt="Figma Icon" class="icon"/></a>
            <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noopener noreferrer"><img src="@/assets/icons/javascript.svg" width="36" height="36" alt="JavaScript Icon" class="icon"/></a>
            <a href="https://www.typescriptlang.org/" target="_blank" rel="noopener noreferrer"><img src="@/assets/icons/typescript.svg" width="36" height="36" alt="TypeScript Icon" class="icon"/></a>
            <a href="https://developer.mozilla.org/en-US/docs/Web/HTML" target="_blank" rel="noopener noreferrer"><img src="@/assets/icons/html.svg" width="36" height="36" alt="HTML Icon" class="icon"/></a>
            <a href="https://flutter.dev/" target="_blank" rel="noopener noreferrer"><img src="@/assets/icons/flutter.svg" width="36" height="36" alt="Flutter Icon" class="icon"/></a>
            <a href="https://vuejs.org/" target="_blank" rel="noopener noreferrer"><img src="@/assets/icons/vue.svg" width="36" height="36" alt="Vue Icon" class="icon"/></a>
        </div>
    </div>
</template>

<style scoped>
@media screen and (max-width: 1024px) {
.about-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    /* padding: 2rem; */
    margin: 2rem;
}
.about-title {
    font-weight: 900;
}
.about-text {
    margin-top: 1rem;
    max-width: 80vw;
}
.icon-wrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem;
    margin-top: 2rem;
}
}

@media screen and (min-width: 1024px) {
.about-section {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    align-items: center;
    padding: 4rem 2rem;
}
.about-title {
    grid-column: 1;
    grid-row: 1 ;
    font-size: 3rem;  
    font-weight: 900;
  }
.about-text {
    grid-column: 1;
    grid-row: 2;
    margin: 0;
}
.icon-wrapper {
    grid-column: 2 / span 2;
    grid-row: 1 / span 3;
    justify-self: center;
    
    margin: 2rem;
    width: 100%;
    max-width: 520px;
}
}
</style>