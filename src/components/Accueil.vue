<script setup lang="ts">
import { ref } from 'vue'

</script>

<template>
  <div id="accueil">
    <div id="banner">
      <h1>Raphael Codewalker</h1>
    </div>
    <div id="content">
      <div id="illustration"></div>
        <div id="presentation">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, nobis ex vitae numquam, 
            quo ut eum debitis enim cumque similique quia omnis. Quas rem corporis quisquam qui? Quisquam, labore non!
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, nobis ex vitae numquam, 
            quo ut eum debitis enim cumque similique quia omnis. Quas rem corporis quisquam qui? Quisquam, labore non!</p>
        </div>    
      </div>
  </div>
</template>



<style scoped>
#accueil{
  position:relative;
  width: 100%;
  height: 100%;
}
#banner {
  background-color: rgb(25, 22, 75);
  width: 100%;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: space-around;
  border-bottom: 5px solid rgb(238, 255, 0);
}
#banner h1 {
  color: rgb(238, 255, 0);
}
#content{
  display: flex;
  width: 100%;
  height: 100%;
}
#presentation{
  width: 40%;
  height: auto;
  margin:auto;
  align-items: center;
}
#presentation p{
  color: yellow;
  font-size: 3em;
  font-variant: 2px;
  letter-spacing: 0.1em;
  line-height: 1em;
}

</style>