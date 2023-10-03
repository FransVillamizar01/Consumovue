<template>
  <div>
    <h1>SI QUIERES IR A LA SIGUIENTE SECCIÓN DALE CLIC AL BOTÓN :D</h1>
    <button @click="openNewTab">Ir a la siguiente sección</button>
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
