<template>
  <div class="character-card">
    <img :src="character.image" :alt="character.name" />
    <p class="character-name">{{ character.name }}</p>
    <div class="character-info">
      <p>Estado: {{ character.status }}</p>
      <p>Especie: {{ character.species }}</p>
      <p>Género: {{ character.gender }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    character: Object,
  },
};
</script>

<style scoped>
.character-card {
  display: inline-block;
  position: relative;
  margin: 25px;
  text-align: center;
  box-shadow: rgba(0, 0, 0, 0.65) 0px 10px 10px;
  border-radius: 10px;
  background-color: white;
  width: 150px;
  overflow: hidden;
  transition: transform 0.65s;
}

.character-card:hover {
  transform: scale(1.1);
}

.character-name {
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
  font-size: 15px;
}

img {
  width: 150px;
  border-radius: 8px;
}

.character-info {
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  color: white;
  font-size: 14px;
  text-align: left;
  padding: 10px;
  box-sizing: border-box;
  border-radius: 0 0 10px 10px;
  opacity: 0;
  transition: top 0.3s ease, opacity 0.3s ease;
}

.character-card:hover .character-info {
  top: 47%;
  opacity: 1;
}
</style>
