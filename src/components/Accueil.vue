<script setup lang="ts">
import { ref } from 'vue'

</script>

<template>
  <div id="accueil">
    <div id="banner">
      <h1>Raphael Codewalker</h1>
    </div>
    <!-- Place in Body where you'd like intro to appear -->
    <div class="presentation">
        <!-- Blue Intro Text -->
        <p class="introduction">
          Not a few days ago, just right now...
        </p>
        <!-- Logo Image or Text goes in here -->
        <h2 class="logo">
          <img src="../assets/codewars.svg">
        </h2>
        <!-- All Scrolling Content Goes in here -->
        <div class="scrolling">
          <div class="texte">
            <p class="titre">Raphael Codewalker<br/>Un nouveau développeur</p>
            <br>
            <p class="paragraphe">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eaque adipisci optio veritatis 
              nobis voluptatibus magni omnis quibusdam quos velit ab. Necessitatibus sed quisquam dolore quibusdam porro numquam repellendus aut sequi?
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eaque adipisci optio veritatis 
              nobis voluptatibus magni omnis quibusdam quos velit ab. Necessitatibus sed quisquam dolore quibusdam porro numquam repellendus aut sequi?
            </p>
            <!-- button or link or whatever -->
            <a href="./StarScroll.zip" class="space-button">Download The Code Now!</a>
          </div>
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

.presentation {
  width: 100%;
  height: 100%;
  font-family: "Droid Sans", arial, verdana, sans-serif;
  font-weight: 700;
  color: #EBD71C;
  overflow: hidden;
  position: absolute;
}

.presentation p.introduction {
  position: relative;
  max-width: 16em;
  font-size: 200%;
  font-weight: 400;
  margin: 20% auto;
  color: #4ee;
  opacity: 0;
  z-index: 1;
  text-align: center;
  -webkit-animation: intro 2s ease-out;
  -moz-animation: intro 2s ease-out;
  -ms-animation: intro 2s ease-out;
  -o-animation: intro 2s ease-out;
  animation: intro 2s ease-out;
}

.presentation .scrolling{
  position: absolute;
  z-index: 3;
  width: 98%;
  margin-left: auto;
  margin-right: auto;
  height: 50em;
  bottom: 0;
  font-size: 150px;
  font-weight: bold;
  text-align: justify;
  overflow: hidden;
  transform-origin: 50% 100%;
  transform: perspective(350px) rotateX(12deg);
  display: flex;
  justify-content: center;
}

.presentation .scrolling:after {
  position: absolute;
  content: ' ';
  top: 0;
  bottom: 60%;
  background-image: linear-gradient(top, rgba(0,0,0,1) 0%, transparent 100%);
  pointer-events: none;
}

.presentation .space-button {
  color: #EBD71C;
  border: 12px solid #EBD71C;
  padding: 20px;
  background: transparent;
  text-decoration: none;
  margin: 0 auto;
  display: block;
  text-align: center;
}

.presentation .space-button:hover {
  background-color: #D2BE03;
  border-color: #D2BE03;
  color: black;
}

.presentation .space-button:active,
.presentation .space-button:focus {
  background-color: #B8A40A;
  border-color: #B8A40A;
  color: black;
}

.presentation .texte {
  position: absolute;
  top: 100%;
  animation: scroll 100s linear 4s forwards infinite ;
  line-height: 1em;
  max-width: 1800px;

}

.presentation .texte > .titre {
  text-align: center;
}
/* Main Image Styles */

.presentation .logo {
  position: absolute;
  width: 2.6em;
  left: 50%;
  top: 20vh;
  font-size: 10em;
  text-align: center;
  margin-left: -1.3em;
  line-height: 0.8em;
  letter-spacing: -0.05em;
  color: #000;
  text-shadow: -2px -2px 0 #EBD71C, 2px -2px 0 #EBD71C, -2px 2px 0 #EBD71C, 2px 2px 0 #EBD71C;
  opacity: 0;
  z-index: 1;
  -webkit-animation: logo 5s ease-out 2.5s;
  -moz-animation: logo 5s ease-out 2.5s;
  -ms-animation: logo 5s ease-out 2.5s;
  -o-animation: logo 5s ease-out 2.5s;
  animation: logo 5s ease-out 2.5s;
}

.presentation .logo > img {
  max-width: 100%;
}

@-webkit-keyframes intro {
  0% { opacity: 1; }
  90% { opacity: 1; }
  100% { opacity: 0; }
}

@-moz-keyframes intro {
  0% { opacity: 1; }
  90% { opacity: 1; }
  100% { opacity: 0; }
}

@-ms-keyframes intro {
  0% { opacity: 1; }
  90% { opacity: 1; }
  100% { opacity: 0; }
}

@-o-keyframes intro {
  0% { opacity: 1; }
  90% { opacity: 1; }
  100% { opacity: 0; }
}

@keyframes intro {
  0% { opacity: 1; }
  90% { opacity: 1; }
  100% { opacity: 0; }
}


@-webkit-keyframes logo {
  0% { -webkit-transform: scale(1); opacity: 1; }
  50% { opacity: 1; }
  100% { -webkit-transform: scale(0.1); opacity: 0; }
}

@-moz-keyframes logo {
  0% { -moz-transform: scale(1); opacity: 1; }
  50% { opacity: 1; }
  100% { -moz-transform: scale(0.1); opacity: 0; }
}

@-ms-keyframes logo {
  0% { -ms-transform: scale(1); opacity: 1; }
  50% { opacity: 1; }
  100% { -ms-transform: scale(0.1); opacity: 0; }
}

@-o-keyframes logo {
  0% { -o-transform: scale(1); opacity: 1; }
  50% { opacity: 1; }
  100% { -o-transform: scale(0.1); opacity: 0; }
}

@keyframes logo {
  0% { transform: scale(1); opacity: 1; }
  50% { opacity: 1; }
  100% { transform: scale(0.1); opacity: 0; }
}

@keyframes scroll {
  0% { top: 100%; }
  100% { top: -150%; }
}

@media screen and (max-width: 720px) {
  .presentation .scrolling {
    font-size: 35px;
  }
  .presentation .texte {
    position: absolute;
    top: 100%;
    animation: scroll 100s linear 4s forwards;
  }
}
@media screen and (max-width: 1400px) {
  .presentation .scrolling {
    font-size: 70px;
  }
  .presentation .texte {
    position: absolute;
    top: 100%;
    animation: scroll 100s linear 4s forwards;
  }
}


</style>