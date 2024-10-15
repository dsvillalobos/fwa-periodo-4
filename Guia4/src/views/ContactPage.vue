<template>
  <div class="contact-page">
    <div class="banner"></div>
    <h1 class="center">Contáctanos</h1>
    <p class="text center">
      Aquí puedes enviar tus consultas o comentarios utilizando el siguiente
      formulario.
    </p>
    <form @submit.prevent="handleSubmit" class="contact-form">
      <div class="form-group">
        <label for="name">Nombre:</label>
        <input type="text" id="name" v-model="name" required />
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />
      </div>
      <div class="form-group">
        <label for="message">Mensaje:</label>
        <textarea id="message" v-model="message" required></textarea>
      </div>
      <button type="submit" class="submit-button">Enviar</button>
      <br />
      <br />
      <br />
      <br />
    </form>
  </div>
</template>

<script>
export default {
  name: "ContactPage",
};
</script>

<style scoped>
.center {
  text-align: center;
}

.text {
  margin: 0px 15% 20px 15%;
  line-height: 30px;
}

.contact-form {
  margin: 0px 15%;
  display: flex;
  flex-direction: column;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

textarea {
  height: 150px;
}

.submit-button {
  background-color: #000;
  color: white;
  padding: 10px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.submit-button:hover {
  background-color: #fff;
  border: 1px solid black;
  color: black;
}

.banner {
  background-image: url("https://images.pexels.com/photos/27203469/pexels-photo-27203469/free-photo-of-a-retail-shopping-store-with-a-lot-of-clothing-and-manikins.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1");
  width: 100%;
  height: 300px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  margin-bottom: 20px;
  filter: grayscale();
}
</style>
