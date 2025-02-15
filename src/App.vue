<template>
  <v-app>
    <div class="love-container">
      <div v-if="showFireworks" class="fireworks"></div>
      <v-container class="texto">
        <v-card class="love-card" elevation="10">
          <v-card-title class="text-center">Feliz Día del Amor 💖</v-card-title>
          <v-card-text class="text-center">Eres la persona más especial en mi vida. ¡Te amo! 💕</v-card-text>
          <v-btn color="pink" dark block @click="triggerFireworks"><i style="font-size: 20px;">Click aquí 😍</i></v-btn>
        </v-card>
      </v-container>
    </div>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      showFireworks: false
    };
  },
  methods: {
    triggerFireworks() {
      this.showFireworks = true;
      setTimeout(() => {
        this.showFireworks = false;
      }, 3000);
    }
  }
};
</script>

<style scoped>
.love-container {
  width: 100%;
  height: 100vh;
  background: url('https://cdn.computerhoy.com/sites/navi.axelspringer.es/public/media/image/2018/02/285357-tarjetas-san-valentin-online-gratis.jpg?tf=1200x') no-repeat center center;
  background-size: cover;
  position: relative;
  overflow: hidden;
}

.fireworks {
  position: absolute;
  width: 100%;
  height: 100%;
  background: url('../public/img/descarga.jpg');
  background-size: cover;
  background-position: center;
  animation: fadeOut 3s ease-in-out;
}

@keyframes fadeOut {
  0% { opacity: 1; }
  100% { opacity: 0; }
}

.love-card {
  max-width: 400px;
  padding: 20px;
  background: white;
  border-radius: 15px;
  text-align: center;
}

.texto {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
