<template>
  
  <p class="p-main"><b>The Rick And Morty Characters</b></p>
  
  <ul class="row justify-content-center">
    <ol class="mr-3 " v-for="(Character, idx) in Characters" :key="idx">
      <br> <div class="div-names">{{ Character.name }}</div> 
      <img class="img-chars" :src="Character.image"/>
      <div class="div-descrip">Description</div>
       Status:  {{ Character.status }} 
       Gender: {{ Character.gender }} <br>
       Origin: {{ Character.origin.name }} <br><br>
    </ol>
  </ul>

  <div class="div-bottom">Project Features: </div>
  <div>-2 components used, First to show the api results, and second to show some messages, button and the main image </div>
  <div>-Consuming Rick and Morty API </div>
  <div>-Use of Vue´s Life cycle (mounted()) </div>
  <div>-Use a for cycle to show the Characters name,image,species,etc   </div>
  <div style="margin-bottom: 40px;">-Style on every component </div>
</template>

<script>
import axios from "axios";

export default {
  name: 'App',
  components: {
  
},
  data() {
    return {
      condtionmessage: "Conditional message should Appear",
      flag:true,
      Characters: null,
    };
  },

  mounted(){
    axios.get("https://rickandmortyapi.com/api/character")
    .then((response) => (this.Characters = response.data.results));
  },
  methods: {
    lowerCase(value) {
      return value.toLowerCase();
    }
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background-color: #03a5fc;
}

h1 {
  color: black;
  font-family: 'Delicious Handrawn', cursive;
  font-size: 150;
}

ul {
  color: white;
  font-family: 'Delicious Handrawn', cursive;
}

p {
  font-size: 50;
  color: black;
  font-family: 'Delicious Handrawn', cursive;
}

.main-img{
  box-shadow: 1px 1px 2px 2px #7a8185;
  border-style: double;
  border-color: #d4d4d4;
  border-width: 14px;
  border-radius: 10%;
  width: 750px;
  margin-bottom: 40px;
  transition: 500ms;

}

.main-img:hover{
  filter: opacity(.5);
  -webkit-transform:scale(1.3);transform:scale(0.8);
  cursor: pointer;
}

.img-chars {
  box-shadow: 1px 1px 2px 2px #7a8185;
  border-style: double;
  border-color: #f5f5f5;
  border-width: 14px;
  width: 300px;
  border-radius: 20%;
  transition: 400ms;
}

.img-chars:hover{
  border-radius: 30%;
  cursor: pointer;
  border-color: #4dfc3e;
  -webkit-transform:scale(1.3);transform:scale(0.9);
  cursor: pointer;
} 

div {
  font-family: 'Delicious Handrawn', cursive;
  font-size: xx-large;
  color: rgba(0, 0, 0, 0.899);
}

.div-names{
  color: #0a1aaa;
  font-weight: bold;
  margin-bottom: 10px;
  
}

.div-names:hover{
  -webkit-transform:scale(1.3);transform:scale(1.5);
  color: #4dfc3e;
  cursor: pointer;
}

.div-descrip:hover{
  -webkit-transform:scale(1.3);transform:scale(1.5);
  cursor: pointer;
  font-weight: 700;
}

.p-main:hover{
  -webkit-transform:scale(1.3);transform:scale(1.5);
  cursor: pointer;
  font-weight: 700;
}

.h1-main:hover{
  -webkit-transform:scale(1.3);transform:scale(1.7);
  cursor: pointer;
  font-weight: 700;
  color: white;
}

.btn-api{
  margin-bottom: 30px;
  background-color: #4dfc3e;
  border-radius: 50%;
  font-size: larger;
  font-weight: bold;
  padding: 14px;
  font-family: 'Delicious Handrawn', cursive;
  border-color: white;
  transition: 500ms;
}

.btn-api:hover{
  background-color: #f1f500;
  -webkit-transform:scale(1.3);transform:scale(0.8);
  cursor: pointer;
}

.div-bottom{
  margin-top: 120px;
  font-size: larger;
  font-weight: bold;
  font-family: 'Delicious Handrawn', cursive;
}

</style>
