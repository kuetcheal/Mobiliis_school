<template>
  <div class="inscription">
    <h1>Formulaire d'Inscription</h1>
    <hr />
    <form @submit.prevent="registerUser">
      <div class="form-group">
        <label for="username">Nom d'utilisateur :</label>
        <input type="text" id="username" name="username" v-model="form.username" required />
      </div>
      <div class="form-group">
        <label for="email">Email :</label>
        <input type="email" id="email" name="email" v-model="form.email" required />
      </div>
      <div class="form-group">
        <label for="phone">Téléphone :</label>
        <input type="tel" id="phone" name="phone" v-model="form.phone" required />
      </div>
      <div class="form-group">
        <label for="password">Mot de passe :</label>
        <input type="password" id="password" name="password" v-model="form.password" required />
      </div>
      <button type="submit">S'inscrire</button>
    </form>

    <footer>
      <p>&copy; 2024 EasyTravel. Tous droits réservés.</p>
    </footer>
  </div>
</template>

<script>

import axios from 'axios';
export default {
  name: 'InscriptionPage',

  data() {
    return {
      form: {
        username: '',
        email: '',
        phone: '',
        password: ''
      }
    };
  },
  methods: {
    async registerUser() {
      try {
        const response = await axios.post('http://localhost:5000/api/register', this.form);
        alert(response.data.message); 
      } catch (error) {
        console.error(error);
        alert('Une erreur est survenue lors de l\'inscription.');
      }
    }
  }
}
</script>

<style scoped>
.inscription {
  max-width: 400px;
  margin: 50px auto;
  padding-bottom: 100px; 
}

h1 {
  text-align: center;
  color: #2c3e50;
  margin-bottom: 10px;
}


hr {
  margin-bottom: 20px;
  border: 0;
  border-top: 2px solid #2c3e50; 
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
  display: inline-block; /* Assure que le label est aligné avec le champ */
  width: 100%; /* Aligne les labels correctement */
}

input {
  width: 100%; /* Chaque input occupe toute la largeur disponible */
  padding: 8px;
  font-size: 1rem;
  box-sizing: border-box; /* Inclut la bordure et le padding dans la taille totale */
}

button {
  width: 100%; /* Le bouton occupe toute la largeur disponible */
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

footer {
  background-color: #6c757d;
  color: white;
  padding: 20px 0;
  text-align: center;
  width: 100%;
  position: fixed; /* Fixer le footer en bas de la page */
  bottom: 0;
  left: 0;
}
</style>
