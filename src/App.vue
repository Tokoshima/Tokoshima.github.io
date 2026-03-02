<script setup>
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <p class="mainMenu">Louw Pretorius</p>
  <p class = "mainMenu">Hi im louw</br>
	jack of all trades, master of a few.</br>
	Here you will find a summary of what i am,</br>
	what i can do, and why i might be worth your time</br>
	</p>
  <a class="mainMenu">About</a>
  <a class="mainMenu">Github</a>
  <a class="mainMenu">Resume</a>
  <a class="mainMenu">Shit</a>
  
  <!-- <HelloWorld msg="Vite + Vue" /> -->
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.mainMenu {
  flex-direction: row;
  padding: 8px 8px 8px 8px;
  margin: 8px 8px 8px 8px;
  background-color:white;
}

</style>
