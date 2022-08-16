<script setup lang="ts">
import { ref } from 'vue'

</script>

<template>
    <div id="nav">
        <div id="buttons">
            <p id="accueil">Accueil</p>
            <p>Mon CV</p>
            <p>Projets Persos</p>
        </div>
        <div id="else"></div>
    </div>
</template>

<style scoped>
#nav {
    display: flex;
    background-color: rgb(18, 20, 53);
    width: 100%;
    height: 50px;
    margin: 0;
    border-bottom: 5px solid rgb(238, 255, 0);
}
#buttons {
    flex: 1;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-left: 10px;
}

#buttons p{
    color: rgb(238, 255, 0);
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    font-size: 1.5em;
}
#buttons p:hover{
    text-shadow: 5px 5px 5px red;
    font-size: 1.8em;
}
#buttons #accueil {
    font-size: 2.6em;
}
#buttons #accueil:hover{
    font-size: 3em;
}
#else {
    flex: 3;
}
</style>