<template>
  <nav>
    <ul>
      <li><router-link to="/">Inicio</router-link></li>
      <li><router-link to="/products">Productos</router-link></li>
      <li><router-link to="/about">Acerca</router-link></li>
      <li><router-link to="/services">Servicios</router-link></li>
      <li><router-link to="/contact">Contacto</router-link></li>
    </ul>
  </nav>
</template>

<style scoped>
body {
  margin: 0;
  padding: 0;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
  background-color: #000;
  display: flex;
  justify-content: center;
}

nav ul li {
  margin: 0;
}

nav ul li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 20px;
  text-decoration: none;
  transition: background-color 0.3s, transform 0.2s;
}

nav ul li a:hover {
  background-color: #fff;
  font-style: italic;
  color: #000;
  transform: scale(1.05);
}

nav ul li a:active {
  background-color: #000;
  color: white;
  transform: scale(0.95);
}
</style>
