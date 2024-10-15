<template>
  <header>
    <img src="@/assets/logo.png" alt="Logo del sitio" class="logo" />
    <h1>Villalobos Shop</h1>
  </header>
</template>

<script>
export default {
  name: "SiteHeader",
};
</script>

<style scoped>
header {
  background: black;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1rem;
}

.logo {
  height: 50px;
  margin-right: 15px;
}

h1 {
  font-family: "Times New Roman", Times, serif;
  font-size: 2em;
  margin: 0;
}
</style>
