<script setup lang="ts"> 
import Card from './Card.vue'
</script>

<template>
    <div class="previous-work-section">
        <h1 class="previous-work-title">Previous Work</h1>
        <div class="cards-wrapper">
            <Card title="Project 1" description="Lorem ipsum dolor sit amet, consectetur adipiscing elit." imageUrl="@/assets/images/project1.png" />
            <Card title="Project 2" description="Lorem ipsum dolor sit amet, consectetur adipiscing elit." imageUrl="@/assets/images/project2.png" />
            <Card title="Project 3" description="Lorem ipsum dolor sit amet, consectetur adipiscing elit." imageUrl="@/assets/images/project3.png" />
        </div>
    </div>
</template>