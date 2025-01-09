<template>
  <nav>
    <div class="logo">GENUIS</div>
    <div class="nav-links">
      <router-link to="/"><i class="fas fa-home"></i> Accueil</router-link>
      <router-link to="/tache"><i class="fas fa-tasks"></i> Tâches</router-link>
    </div>
    <div>
      <router-link to="/compte"
        ><i class="fas fa-user"></i> Mon compte</router-link
      >
    </div>
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px;
  box-shadow: 0 8px 12px rgba(0, 0, 0, 0.1);
}

.logo {
  font-weight: bold;
  font-size: 24px;
}

.nav-links {
  display: flex;
  gap: 20px;
}

nav a {
  color: #030d17;
  text-decoration: none;
  font-weight: bold;
}
nav a:hover {
  color: #ffd700;
}

nav a.router-link-exact-active {
  color: #0056b3;
}
</style>
