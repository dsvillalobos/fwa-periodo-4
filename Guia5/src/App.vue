<template>
  <div style="background-color: #f2e8cf !important">
    <h1 class="lilita-one-regular">Rick and Morty Characters</h1>

    <CharacterFilter @filter-change="applyFilters" />

    <div v-if="characters.length === 0">Loading characters...</div>
    <div class="characters-container">
      <CharacterCard
        v-for="character in filteredCharacters"
        :key="character.id"
        :character="character"
      />
    </div>

    <CharacterPagination
      :prevPage="prevPage"
      :nextPage="nextPage"
      @paginate="fetchCharacters"
    />
  </div>
</template>

<script>
import axios from "axios";
import CharacterCard from "./components/CharacterCard.vue";
import CharacterFilter from "./components/CharacterFilter.vue";
import CharacterPagination from "./components/CharacterPagination.vue";

export default {
  components: {
    CharacterCard,
    CharacterFilter,
    CharacterPagination,
  },
  data() {
    return {
      characters: [],
      nextPage: null,
      prevPage: null,
      searchQuery: "",
      selectedStatus: "",
      filteredCharacters: [],
    };
  },
  mounted() {
    this.fetchCharacters("https://rickandmortyapi.com/api/character");
  },
  methods: {
    async fetchCharacters(url) {
      try {
        const response = await axios.get(url);
        this.characters = response.data.results;
        this.nextPage = response.data.info.next;
        this.prevPage = response.data.info.prev;
        this.applyFilters();
      } catch (err) {
        console.log("Error fetching characters: ", err);
      }
    },
    applyFilters({ searchQuery = "", selectedStatus = "" } = {}) {
      this.filteredCharacters = this.characters.filter((character) => {
        const matchesName = character.name
          .toLowerCase()
          .includes(searchQuery.toLowerCase());
        const matchesStatus =
          selectedStatus === "" ||
          character.status.toLowerCase() === selectedStatus;
        return matchesName && matchesStatus;
      });
    },
  },
};
</script>

<style scoped>
h1 {
  margin: 0;
  padding: 20px 0;
  text-align: center;
  font-family: Arial, Helvetica, sans-serif;
  color: #000;
  font-size: 40px;
}

.characters-container {
  text-align: center;
  min-height: 400px;
  padding: 20px 0;
  background-color: #f2e8cf;
}

.lilita-one-regular {
  font-family: "Lilita One", sans-serif;
  font-weight: 400;
  font-style: normal;
}
</style>
