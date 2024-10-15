<template>
  <main>
    <h2>Galería de Villalobos Shop</h2>
    <div class="image-gallery">
      <img
        v-for="(image, index) in images"
        :key="index"
        :src="image"
        :alt="`Imagen ${index + 1}`"
      />
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      images: [
        "https://i.pinimg.com/736x/b6/0d/30/b60d30750f4725fb54d86fba79eec8d5.jpg",
        "https://i.pinimg.com/736x/e7/de/a9/e7dea960c69d06e5f2997a7ca3ae1308.jpg",
        "https://i.pinimg.com/564x/30/3b/fe/303bfe2f737b0d14d24de57e52fbab7b.jpg",
        "https://i.pinimg.com/736x/57/18/2b/57182b2baca22539126e961586352f2e.jpg",
        "https://i.pinimg.com/736x/e8/be/96/e8be960fd79e12a78d527c90d8337e24.jpg",
        "https://i.pinimg.com/564x/42/79/6c/42796c83c9a2a570be9631e4b32d319f.jpg",
        "https://i.pinimg.com/564x/6f/bf/eb/6fbfebf8b2d7b9e47c66eba5dd6b9e4b.jpg",
        "https://i.pinimg.com/564x/cd/5b/4a/cd5b4a4949f5c89f80fed4c7e804c3ac.jpg",
        "https://i.pinimg.com/736x/47/ad/72/47ad728459ea9ddd2b28399d0adc97b2.jpg",
        "https://i.pinimg.com/736x/c2/2e/2f/c22e2fb11f165db21542170d1e8f4219.jpg",
      ],
    };
  },
};
</script>

<style scoped>
main {
  padding: 20px;
  margin: 0;
  padding-bottom: 60px;
  margin-bottom: 70px;
}

.image-gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin-top: 20px;
}

.image-gallery img {
  margin: 10px;
  max-width: 300px;
  height: 300px;
  object-fit: cover;
  object-position: center;
  border-radius: 7px;
}
</style>
