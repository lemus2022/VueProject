<template>
    <h1 class="h1-main">{{ messagewelcome }}</h1>
    <p>{{ messageautor }}</p>
    <img alt="Main img" class="main-img" src="../assets/main.jpg"><br>  
    <a href="https://rickandmortyapi.com/" target="_blank"><button class="btn-api">{{ messagebtn }}</button></a>
    <p>{{ conditional }}</p>

</template>

<script>
export default {
name: 'SecondaryComponent',
props: {
  messagebutton: String,
  conditional: String

},
data() {
    return {
      messagebtn: "Visit API Website",
      messagewelcome: "Welcome",
      messageautor: "The Rick And Morty API by Alejandro Lemus",
      
    };
  }
}
</script>

<style scoped>
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
}

</style>
