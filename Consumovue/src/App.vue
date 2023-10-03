<template>
  <div class="container">
    <div class="center-vertically">
      <h1 class="title">SI QUIERES IR A LA SIGUIENTE SECCIÓN DALE CLIC AL BOTÓN :D</h1>
      <button class="button" @click="openNewTab">Ir a la siguiente sección</button>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'App',
  setup() {
    const nextPageUrl = ref('/PagCarts'); // Cambia '/PagCarts' a la URL deseada

    const openNewTab = () => {
      window.open(nextPageUrl.value, '_blank');
    };

    return {
      nextPageUrl,
      openNewTab,
    };
  },
}
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.center-vertically {
  text-align: center;
}

.title {
  font-size: 2rem;
  margin-bottom: 20px;
}

.button {
  padding: 1rem 1rem;
  background-color: #ff0000;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 18px;
  transition: background-color 0.3s;
}

.button:hover {
  background-color: #0056b3;
}

/* Estilo para cuando se hace clic en el botón */
.button:active {
  background-color: #004399;
}
</style>
