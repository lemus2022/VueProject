<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Message from HelloWorld"/> -->
  <Homework v-if="isSentence" :msgc="message4" />
  <b><Homework v-false ="isSentence" :msg="message" :msgg="message2" :msggg="message3" /></b>
  <p><b>The Rick And Morty Characters</b></p>
 
  <ul>
    <ol v-for="(Character, idx) in Characters" :key="idx">
      <br> {{ Character.name }} <br>
      <img class="img-chars" :src="Character.image"/>
    </ol>
  </ul>

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import Homework from './components/Homework.vue';
import axios from "axios";

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Homework
  },
  data() {
    return {
      message: "Welcome",
      message2: "The Rick And Morty API",
      message3: "Visit website",
      message4: "Conditional message",
      isSentence: false,
      wonders: ["CHICHEN ITZA", "CHRIST THE REDEEMER", "TAJ MAHAL", "GREAT WALL OF CHINA", "MACHU PICCHU", "PETRA", "COLOSSEUM"],
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

}
.img-chars {
  box-shadow: 1px 1px 2px 2px #7a8185;
  border-style: double;
  border-color: #f5f5f5;
  border-width: 14px;
  width: 300px;
  border-radius: 20%;
}

/* img:hover{
  border-radius: 30%;
  cursor: pointer;
  width: 400px;
} */

div {
  font-family: 'Delicious Handrawn', cursive;
  font-size: xx-large;
  color: rgba(0, 0, 0, 0.899);
}

button {
  background-color: #086308;
  width: 200px;
  height: 50px;
  font-size: x-large;
  color: white;
  border: white;
  border-radius: 50%;
  font-weight: 300;
  font-family: 'Delicious Handrawn', cursive;
}

button:hover {
  background-color: #48db48;
  width: 180px;
  height: 50px;
  font-size: x-large;
  color: black;
  border: white;
  border-radius: 50%;
  cursor: pointer;
}

</style>
