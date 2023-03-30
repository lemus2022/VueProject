<template>
        <h1 class="h1-main">{{ msg }}</h1>
        <p>{{ msgg }}</p>
        <img alt="Main img" class="main-img" src="../assets/main.jpg">     
        <h2>{{ msgc }}</h2>
        <a href="https://rickandmortyapi.com/" target="_blank"><button class="btn-api">{{ msggg }}</button></a>
  
  </template>
  
  <script>
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Project',
    props: {
      msg: String,
      msgg: String,
      msggg: String,
      msgc: String,

    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  
  </style>
  