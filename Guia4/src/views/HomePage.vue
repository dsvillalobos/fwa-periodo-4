<template>
  <div class="home-page">
    <div class="banner">
      <br /><br />
      <h1 class="banner-title">
        ¡Bienvenido a
        <span class="serif">Villalobos Shop</span>!
      </h1>
    </div>
    <MainContent />
  </div>
</template>

<script>
import MainContent from "@/components/MainContent.vue";

export default {
  name: "HomePage",
  components: {
    MainContent,
  },
};
</script>

<style scoped>
.serif {
  font-family: "Times New Roman", Times, serif;
}

.text {
  margin: 0px 2% 0px 2%;
  line-height: 25px;
  text-align: left;
}

.home-page {
  text-align: center;
}

.banner {
  background-color: #f8f9fa;
  color: white;
  margin-bottom: 30px;
  padding: 20px 0;
  background-image: url("https://images.pexels.com/photos/19599230/pexels-photo-19599230/free-photo-of-a-store-with-many-clothes-on-display-and-mannequins.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1");
}

.banner-title {
  display: inline-block;
  padding: 20px;
  background-color: black;
  color: white;
}

.features {
  display: flex;
  justify-content: center;
  gap: 40px;
}

.feature-card {
  background-color: #000;
  color: white;
  border-radius: 8px;
  padding: 15px;
  width: 200px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}

.feature-card:hover {
  transform: translateY(-5px);
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
  gap: 50px;
}

.gallery-item img {
  width: 100%;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  object-position: center;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}

.gallery-item img:hover {
  transform: scale(1.05);
}
</style>
