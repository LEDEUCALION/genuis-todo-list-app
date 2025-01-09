<template>
  <div id="app">
    <header class="header">
      <h1>Bienvenue sur My Todo List App</h1>
      <p>Gérez vos tâches facilement et efficacement.</p>
    </header>
    <section>
      <h2>Fonctionnalités</h2>
      <div class="detail-fonctionnalite">
        <Task v-for="task in tasks" :key="task.id" :task="task" />
      </div>
    </section>
    <div class="btn-inscription">
      <h2>S'inscrire</h2>
      <p>Créez un compte pour commencer à gérer vos tâches.</p>
      <button>S'inscrire</button>
    </div>
    <div class="btn-connexion">
      <h2>Se connecter</h2>
      <p>Connectez-vous à votre compte pour accéder à vos tâches.</p>
      <button>Se connecter</button>
    </div>
  </div>
</template>

<script>
import Task from "@/components/Task.vue";
export default {
  name: "HomeView",
  components: { Task },
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: "Créer des tâches",
          image: "./src/assets/images/ajouter.jpg",
          description: "Ajoutez de nouvelles tâches à la liste des taches .",
        },
        {
          id: 2,
          title: "supprimer des tâches",
          image: "@/images/supprimer.jpg",
          description: "supprimez des tâches qui ne sont plus nécessaires.",
        },
        {
          id: 3,
          title: "modifier vos tâches",
          image: "frontend/my-todo-list-app/src/assets/images/modifier.jpg",
          description: "Mettez à jour les informations d'une tâche existante.",
        },
        {
          id: 4,
          title: "Visualiser vos tâches",
          image: "../assets/images/visualiser.jpg",
          description: "Visualisez vos tâches grâce à des graphiques.",
        },
      ],
    };
  },
};
</script>

<style scoped>
body {
  font-family: Arial, sans-serif;
  background-color: #f0f0f0;
  color: #333;
}

.header {
  text-align: center;
  padding: 2rem;
  background-color: #007bff;
  color: #fff;
}

section h2 {
  padding: 2rem;
  background-color: #fff;
}

.detail-fonctionnalite {
  background-color: #f0f0f0;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(129, 44, 44, 0.1);
}

.btn-inscription,
.btn-connexion {
  text-align: center;
  padding: 2rem;
  background-color: #fff;
}

button {
  background-color: #0056b3;
  color: #fff;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 50px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #ebe23f;
  color: #0056b3;
}
</style>
