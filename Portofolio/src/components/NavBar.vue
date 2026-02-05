<script setup lang="ts">
import { ref } from 'vue'

const open = ref(false)
function toggle() {
    open.value = !open.value
}
</script>

<template>
    <header>
        <h1 class="H-name">Robin van Barneveld</h1>

        <button
            class="menu-button"
            :aria-expanded="open"
            aria-label="Toggle navigation"
            @click="toggle"
        >
            <svg width="32" height="32" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
                <path d="M3 6h18M3 12h18M3 18h18" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
        </button>

        <nav class="navbar" :class="{ 'open': open }">
            <a href="#about" @click="open = false">About</a>
            <a href="#projects" @click="open = false">Projects</a>
            <a href="#contact" @click="open = false">Contact</a>
        </nav>
    </header>
</template>

<style scoped>
.H-name {
    font-size: 2.25rem;
    font-weight: bold;
    margin: 0;
    color: #ffffff;
}

/* Desktop: show nav links inline */
.navbar {
    display: flex;
    gap: 1rem;
    margin-top: 0.5rem;
}
.navbar a {
    text-decoration: none;
    font-weight: 500;
}
.navbar a:hover {
    color: #007BFF;
}

/* Menu button - hidden on large screens */
.menu-button {
    background: transparent;
    border: none;
    padding: 0.25rem;
    margin-left: 0.5rem;
    display: none; /* hidden by default, shown on small screens */
    cursor: pointer;
}

/* Mobile styles */
@media (max-width: 1024px) {
    .menu-button {
        display: inline-flex;
        align-items: center;
    }

    .H-name {
        font-size: 1.75rem;
    }

    /* Hide desktop inline nav on mobile; we'll show a stacked dropdown when open */
    .navbar {
        display: none;
        flex-direction: column;
        gap: 0.5rem;
        margin-top: 0.5rem;
        background: var(--color-background);
        padding: 0.75rem 1rem;
        border-radius: 6px;
        box-shadow: 0 6px 18px rgba(0,0,0,0.06);
        position: absolute;
        right: 1rem;
        top: 3.5rem;
        min-width: 160px;
        z-index: 50;
    }

    /* When open, show the mobile dropdown */
    .navbar.open {
        display: flex;
    }

    /* Make links easier to tap on mobile */
    .navbar a {
        padding: 0.5rem 0.25rem;
    }

    /* Stack header layout: keep title and button on same row */
    header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        position: relative; 
        padding: 0.25rem 0;
    }
}

/* Desktop header layout */
@media (min-width: 1024px) {
    header {
        display: flex;
        padding: 0.625rem 1.25rem;
        justify-content: space-between;
        align-items: center;
    }
    .menu-button { display: none; }
    .H-name { padding-right: 15rem; }
    .navbar {
        display: flex;
        flex: 1;
        justify-content: space-around;
        align-items: center;
        margin: 0;
    }
    .navbar a { font-size: 1.3rem; padding: 0 0.5rem; }
}

</style>