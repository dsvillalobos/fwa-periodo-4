<template>
  <div class="products-page">
    <h1>Productos de {{ brandName }}</h1>

    <div class="filter">
      <label for="category">Filtrar por categoría: </label>
      <select v-model="selectedCategory" id="category">
        <option value="">Todas</option>
        <option
          v-for="category in uniqueCategories"
          :key="category"
          :value="category"
        >
          {{ category }}
        </option>
      </select>

      <label for="date">Ordenar por fecha: </label>
      <select v-model="sortByDate" id="date">
        <option value="">Ninguno</option>
        <option value="newest">Más reciente</option>
        <option value="oldest">Más antiguo</option>
      </select>

      <label for="popularity">Ordenar por popularidad: </label>
      <select v-model="sortByPopularity" id="popularity">
        <option value="">Ninguno</option>
        <option value="most">Más popular</option>
        <option value="least">Menos popular</option>
      </select>
    </div>

    <div class="gallery">
      <h2>Galería de Productos</h2>
      <div class="gallery-grid">
        <div
          class="gallery-item"
          v-for="(product, index) in filteredProducts"
          :key="index"
        >
          <img :src="product.image" :alt="product.name" />
          <h3>{{ product.name }}</h3>
          <p>{{ product.price }}</p>
          <p>Fecha: {{ product.date }}</p>
          <p>Popularidad: {{ product.popularity }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductsPage",
  data() {
    return {
      brandName: "Villalobos Shop",
      selectedCategory: "",
      sortByDate: "",
      sortByPopularity: "",
      products: [
        {
          name: "Hoodie de Algodón",
          category: "Ropa",
          price: "$20",
          image:
            "https://i.pinimg.com/564x/54/e1/87/54e1874b496d95290a267cdda2d42f4d.jpg",
          date: "2023-09-01",
          popularity: 80,
        },
        {
          name: "Baggy Jeans",
          category: "Ropa",
          price: "$30",
          image:
            "https://i.pinimg.com/736x/b3/85/e6/b385e60602d225ebfa2fba7cd8939e15.jpg",
          date: "2023-08-15",
          popularity: 95,
        },
        {
          name: "NIKE Air Force Ones",
          category: "Calzado",
          price: "$50",
          image:
            "https://i.pinimg.com/564x/70/81/10/70811021e8f389fab093ad7b21cf4d9b.jpg",
          date: "2023-09-20",
          popularity: 60,
        },
        {
          name: "Gucci Bag",
          category: "Accesorios",
          price: "$100",
          image:
            "https://i.pinimg.com/564x/6f/ae/8c/6fae8cc1bcfce9044957581d1378708e.jpg",
          date: "2023-07-10",
          popularity: 70,
        },
      ],
    };
  },
  computed: {
    uniqueCategories() {
      const categories = this.products.map((product) => product.category);
      return [...new Set(categories)];
    },

    filteredProducts() {
      let filtered = [...this.products];

      if (this.selectedCategory) {
        filtered = filtered.filter(
          (product) => product.category === this.selectedCategory
        );
      }

      if (this.sortByDate === "newest") {
        filtered.sort((a, b) => new Date(b.date) - new Date(a.date));
      } else if (this.sortByDate === "oldest") {
        filtered.sort((a, b) => new Date(a.date) - new Date(b.date));
      }

      if (this.sortByPopularity === "most") {
        filtered.sort((a, b) => b.popularity - a.popularity);
      } else if (this.sortByPopularity === "least") {
        filtered.sort((a, b) => a.popularity - b.popularity);
      }

      return filtered;
    },
  },
};
</script>

<style scoped>
.products-page {
  text-align: center;
  margin: 20px;
}

.filter {
  margin: 20px 0;
}

.gallery {
  margin-top: 40px;
}

.gallery h2 {
  margin-bottom: 20px;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
}

.gallery-item img {
  width: 300px;
  height: 200px;
  object-fit: cover;
  object-position: center;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}

.gallery-item img:hover {
  transform: scale(1.05);
}

.gallery-item {
  text-align: center;
}
</style>
