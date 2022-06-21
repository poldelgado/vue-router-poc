<template>
    <nav id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/brazil">Brazil</router-link> |
        <router-link to="/panama">Panama</router-link> |
        <router-link to="/hawaii">Hawaii</router-link> |
        <router-link to="/jamaica">Jamaica</router-link>


    </nav>
</template>

<style scoped>
    #nav {
        display: flex;
        justify-content: center;
        padding: 30px;
    } 
    #nav a {
    color: #2c3e50;
    text-decoration: none;
    font-weight: bold;
    }
    #nav a.vue-school-active-class {
    color: #ab26ab;
    }
</style>