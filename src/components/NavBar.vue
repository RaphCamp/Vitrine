<script setup lang="ts">
import { ref } from 'vue'
const hamburgerToggler = document.querySelector<HTMLElement>(".hamburger");
const navLinksContainer = document.querySelector<HTMLElement>(".navlinks-container");
if(hamburgerToggler && navLinksContainer){
    const toggleNav = () => {
    hamburgerToggler.classList.toggle("open")

    const ariaToggle = hamburgerToggler.getAttribute("aria-expanded") === "true" ?  "false" : "true";
    hamburgerToggler.setAttribute("aria-expanded", ariaToggle)

    navLinksContainer.classList.toggle("open")
        
    }
    hamburgerToggler.addEventListener("click", toggleNav)

    new ResizeObserver(entries => {
    if(entries[0].contentRect.width <= 900){
        navLinksContainer.style.transition = "transform 0.3s ease-out"
    } else {
        navLinksContainer.style.transition = "none"
    }
    }).observe(document.body)
}
</script>

<template>
<nav>

      <a href="#" class="nav-icon" aria-label="visit homepage" aria-current="page">
        <img src="../assets/codewars.svg" alt="chat icon">
        <span>Raphaël Codewalker</span>
      </a>

      <div class="main-navlinks">
        <button class="hamburger" type="button" aria-label="Toggle navigation" aria-expanded="false">
          <span></span>
          <span></span>
          <span></span>
        </button>
        <div class="navlinks-container">
          <a href="#" aria-current="page">Accueil</a>
          <a href="#">Mon CV</a>
          <a href="#">Projets Perso</a>
          <a href="#">Sites</a>
          <a href="#">Contact</a>
        </div>
      </div>

      <div class="nav-authentication">
        <a href="#" class="sign-user" aria-label="Sign in page">
          <img src="../assets/stormtrooper.svg" alt="user-icon">
        </a>
        <div class="sign-btns">
          <button type="button">Sign In</button>
          <button type="button">Sign Up</button>
        </div>
      </div>
    </nav>
</template>

<style scoped>

nav {
  width: 100%;
  display: flex;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  align-items: center;
  padding: 15px 25px;
  background-color: rgb(37, 40, 105);
  border-bottom: 5px solid rgb(238, 255, 0);
  box-shadow: inset 0px -1px 0px #c5c5c6;
}

.nav-icon {
  display: flex;
  align-items: center;
  text-decoration: none;
  margin-right: 20px;
}

.nav-icon span {
  font-family: Roboto Flex, sans-serif;
  font-size: 2.6em;
  margin-left: 10px;
  font-weight: 400;
  color: rgb(238, 255, 0);
}
.nav-icon img {
  width: 90px;
  transform: rotate(-17deg) translateX(5px);
}
.hamburger {
  display: none;
}
.navlinks-container a {
  margin: 0 10px;
  font-weight: 500;
  text-decoration: none;
  color: #414141;
  display: inline-block;
  position: relative;
  color: rgb(238, 255, 0);
  font-size: 1.5em;
}
.navlinks-container a::after {
  content: "";
  display: block;
  position: absolute;
  bottom: -6px;
  width: 100%;
  height: 6px;
  transform: scaleX(0);
  transform-origin: left;
  background: rgb(226, 212, 14);
  transition: transform 0.3s ease-out;
}

.navlinks-container a:hover::after {
  transform: scaleX(1)
}

.nav-authentication {
  margin-left: auto;
}

.sign-btns button {
  font-size: 16px;
  min-width: 90px;
  padding: 10px 5px;
  margin: 0 5px;
  border-radius: 5px;
  cursor: pointer;
  border: none; 
}

.sign-btns button:nth-child(2) {
  border: none;
  background: #92c3eeb7;
}
.sign-user {
  display: none;
}

@media (max-width: 900px) {
  nav {
    padding: 15px 20px;
    position: relative;
  }

  .nav-icon {
    order: 2;
    margin: 0 auto;
  }

  .nav-icon span {
    font-size: 22px;
  }

  .main-navlinks {
    order: 1;
  }
  /* Hamburger */
  .hamburger {
    width: 20px;
    height: 20px;
    cursor: pointer;
    border: none;
    display: flex;
    background: #fafafa;
    align-items: center;
    position: relative;
  }
  .hamburger span {
    display: block;
    width: 100%;
    height: 2px;
    background: #333;
    position: absolute;
    pointer-events: none;
    transition: opacity 0.3s 0.15s ease-out;
  }
  .hamburger span:nth-child(1),
  .hamburger span:nth-child(3) {
    transition: transform 0.3s ease-out;
  }
  .hamburger span:nth-child(1) {
    transform: translateY(7px);
  }
  .hamburger span:nth-child(3) {
    transform: translateY(-7px);
  }
  .hamburger.open span:nth-child(1) {
    transform: translate(0) rotate(135deg);
  }
  .hamburger.open span:nth-child(2) {
    opacity: 0;
    transition: opacity 0s ease-out;
  }
  .hamburger.open span:nth-child(3) {
    transform: translate(0) rotate(-135deg);
  }

  .navlinks-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    position: absolute;
    background: #fafafa;
    top: 100%;
    left: 0;
    height: 100vh;
    padding: 15px 50px 15px 20px;
    border-right: 1px solid #c5c5c6;
    transform: translate(-100%);
  }
  .open {
    transform: translate(0%);
  }
  .navlinks-container a {
    font-size: 18px;
    margin: 10px 0
  }

  .nav-authentication {
    order: 3;
    margin-left: 0;
  }
  .sign-btns {
    display: none;
  }
  .sign-user {
    display: block;
    cursor: pointer;
    border: none;
  }
  .sign-user img {
    width: 30px;
}

}

@media (max-width: 500px) {
  .nav-icon img {
    width: 30px;
  }
  .nav-icon span {
    font-size: 20px;
  }
}

</style>