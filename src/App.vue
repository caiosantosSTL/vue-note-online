<script setup>
import NoteVue from "./components/Note.vue";
</script>

<template>
  <div class="nav">
    <div>
      <h1>My fast Note 📒</h1>
      
    </div>
  </div>
  <div class="container">
    <NoteVue />
  </div>
  <div class="footer">
    <p>This project was created with 💛 using Vue3</p>
  </div>
</template>

<style>
* {
  margin: 0;
  
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.nav {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: rgb(14, 14, 14);
  height: 150px;
  margin-bottom: 20px;
  color: rgb(255, 255, 255);
}

.footer {
  background-color: rgb(14, 14, 14);
  height: 100px;
  margin-top: 20px;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-inline: 50px;
  min-width: 300px;
  height: 100vh;
}
</style>
