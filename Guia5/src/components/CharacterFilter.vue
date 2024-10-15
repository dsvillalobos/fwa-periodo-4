<template>
  <div class="search-filter">
    <input
      type="text"
      v-model="searchQuery"
      placeholder="Buscar por nombre..."
      @input="$emit('filter-change', { searchQuery, selectedStatus })"
    />
    <select
      v-model="selectedStatus"
      @change="$emit('filter-change', { searchQuery, selectedStatus })"
    >
      <option value="">Todos los estados</option>
      <option value="alive">Vivo</option>
      <option value="dead">Muerto</option>
      <option value="unknown">Desconocido</option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchQuery: "",
      selectedStatus: "",
    };
  },
};
</script>

<style scoped>
.search-filter {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: 20px;
}

input[type="text"],
select {
  padding: 10px;
  border-radius: 5px;
  font-size: 16px;
  outline: none;
  width: 30%;
}
</style>
