<script setup lang="ts">
import { ref } from 'vue'

</script>

<template>
    <div class="nav">
        <div class="buttons">
            <p id="accueil">Accueil</p>
            <p>Mon CV</p>
            <p>Projets Persos</p>
        </div>
        <div id="else"></div>
    </div>
</template>

<style scoped>
.nav {
    display: flex;
    background-color: rgb(179, 19, 19);
    width: 100%;
    height: 50px;
    margin: 0;
    border-bottom: 5px solid rgb(66, 60, 60);
}
.buttons {
    flex: 1;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-left: 10px;
}

.buttons p{
    color: aliceblue;
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    font-size: 1.5em;
}
#accueil {
    font-size: 2.6em;
}
#else {
    flex: 3;
}
</style>