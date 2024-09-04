<template>
    <div class="connexion">
      <h1>Connexion</h1>
      <hr />
      <form>
        <div class="form-group">
          <label for="email">Email :</label>
          <input type="email" id="email" name="email" required />
        </div>
        <div class="form-group">
          <label for="password">Mot de passe :</label>
          <input type="password" id="password" name="password" required />
        </div>
        <button type="submit">Se connecter</button>
      </form>
  
      <div class="links">
        <p>Pas encore inscrit ? <a href="/inscription"> Inscrivez-vous</a></p>
        <p><a href="/resetPassword">Mot de passe oublié ?</a></p>
      </div>
  
      <footer>
        <p>&copy; 2024 EasyTravel. Tous droits réservés.</p>
      </footer>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ConnexionPage',
  }
  </script>
  
  <style scoped>
  .connexion {
    max-width: 400px;
    margin: 50px auto;
    padding-bottom: 100px; /* Pour éviter que le formulaire chevauche le footer */
  }
  
  h1 {
    text-align: center;
    color: #2c3e50;
    margin-bottom: 10px;
  }
  
  hr {
    margin-bottom: 20px;
    border: 0;
    border-top: 2px solid #2c3e50; /* Ligne horizontale */
    width: 80%;
    margin-left: auto;
    margin-right: auto;
  }
  
  form {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .form-group {
    width: 100%;
    margin-bottom: 15px;
  }
  
  label {
    margin-bottom: 5px;
    font-weight: bold;
    display: inline-block;
    width: 100%;
  }
  
  input {
    width: 100%;
    padding: 8px;
    font-size: 1rem;
    box-sizing: border-box;
  }
  
  button {
    width: 100%;
    padding: 10px;
    background-color: #2c3e50;
    color: white;
    border: none;
    cursor: pointer;
    font-size: 1rem;
    margin-top: 10px;
  }
  
  button:hover {
    background-color: #34495e;
  }
  
  /* Styles pour les liens */
  .links {
    margin-top: 20px;
    text-align: center;
  }
  
  .links a {
    color: #2c3e50;
    text-decoration: none;
  }
  
  .links a:hover {
    text-decoration: underline;
  }
  
  footer {
    background-color: #6c757d;
    color: white;
    padding: 20px 0;
    text-align: center;
    width: 100%;
    position: fixed;
    bottom: 0;
    left: 0;
  }
  </style>
  