<template>
  <div class="introuvable">
    <div class="erreur">
      <div class="erreur-404">404</div>
      <p class="erreur-message">
        Oups! La page que vous recherchez est introuvable.
      </p>
      <p class="retour">
        Redirection vers la page d'accueil dans {{ countdown }} secondes...
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "NotFound",
  data() {
    return {
      countdown: 10,
    };
  },
  created() {
    this.startCountdown();
  },
  methods: {
    startCountdown() {
      const interval = setInterval(() => {
        if (this.countdown > 0) {
          this.countdown--;
        } else {
          clearInterval(interval);
          this.redirectToHome();
        }
      }, 1000);
    },
    redirectToHome() {
      this.$router.push("/");
    },
  },
};
</script>

<style scoped>
.introuvable {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(to bottom, #000428, #004e92);
  color: white;
  text-align: center;
  font-family: "Arial", sans-serif;
  position: relative;
  overflow: hidden;
}

.erreur {
  animation: fadeIn 2s ease-in-out;
}

.erreur-404 {
  font-size: 10rem;
  font-weight: bold;
}

.erreur-message,
.retour {
  font-size: 1.5rem;
  margin-top: 1rem;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

body {
  background: url("https://example.com/dark-blue-sky-with-stars.jpg") no-repeat
    center center fixed;
  background-size: cover;
}
</style>
