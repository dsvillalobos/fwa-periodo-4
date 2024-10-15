<template>
  <div class="pagination-buttons">
    <button @click="$emit('paginate', prevPage)" :disabled="!prevPage">
      Anterior
    </button>
    <button @click="$emit('paginate', nextPage)" :disabled="!nextPage">
      Siguiente
    </button>
  </div>
</template>

<script>
export default {
  props: {
    prevPage: String,
    nextPage: String,
  },
};
</script>

<style scoped>
.pagination-buttons {
  text-align: center;
  margin-top: 20px;
  padding-bottom: 20px;
}

button {
  padding: 10px 20px;
  margin: 5px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
  border: none;
  background-color: #333;
  color: white;
}

button:disabled {
  background-color: #888;
  cursor: not-allowed;
}
</style>
