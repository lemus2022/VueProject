<template>
      <h1>{{ msg }}</h1>
      <p>{{ msgg }}</p>
      <img alt="Vue logo" class="main-img" src="../assets/main.jpg"><br>
        <!-- <a href="https://www.nytimes.com/2017/12/21/reader-center/seven-wonders-world-readers-react.html"><button>{{ msggg }}</button></a>
         -->
        <h2>{{ msgc }}</h2>

  </template>
  
  <script>
  export default {
    name: 'HelloWorld',
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
  