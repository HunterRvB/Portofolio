<script setup lang="ts">
defineProps<{
  title: string
    imageUrl: string
}>()
</script>

<template>
  <div class="card">
    <img :src="imageUrl" alt="Project Image" class="card-image" />
    <div class="card-content">
      <h3 class="card-title">{{ title }}</h3>
    </div>
  </div>
</template>

<style scoped>
.card { 
    display: flex;  
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin: 1rem;
    padding: 1rem;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    background-color: #fff;
    color: #000;
    
}
.card-title {
    font-size: 1.5rem;
    font-weight: 700;
}
</style>