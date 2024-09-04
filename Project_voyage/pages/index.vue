<template>
    <div class="home">
      <h1>Bienvenue sur notre site !</h1>
      <p>Nous sommes ravis de vous accueillir sur notre plateforme.</p>
      <nuxt-link to="/inscription">Aller à la page d'inscription</nuxt-link>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomePage',
  }
  </script>
  
  <style scoped>
  .home {
    text-align: center;
    margin-top: 50px;
  }
  
  h1 {
    color: #2c3e50;
    font-size: 3rem;
  }
  
  p {
    color: #34495e;
    font-size: 1.2rem;
  }
  
  nuxt-link {
    display: inline-block;
    margin-top: 20px;
    color: #3498db;
    text-decoration: none;
    font-weight: bold;
  }
  
  nuxt-link:hover {
    text-decoration: underline;
  }
  </style>
  