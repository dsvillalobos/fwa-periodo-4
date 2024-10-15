<template>
  <div class="services-page">
    <div class="banner"></div>
    <h1 class="center">Nuestros Servicios</h1>
    <p class="text">
      En Villalobos, entendemos que cada cliente es único y, por ello, ofrecemos
      una gama de servicios diseñados para proporcionar una experiencia
      excepcional. Nuestro equipo de expertos está disponible para brindar
      asesoría personalizada, ayudándote a encontrar las piezas perfectas que se
      adapten a tu estilo y necesidades. Además, ofrecemos servicios de
      sastrería y ajustes a medida, asegurando que cada prenda se ajuste
      perfectamente a tu figura. Para aquellos que buscan un toque aún más
      exclusivo, contamos con un servicio de estilismo privado, donde podrás
      disfrutar de sesiones personalizadas en un ambiente íntimo y sofisticado.
      En Villalobos, nuestra misión es hacer que cada visita sea memorable y que
      te sientas verdaderamente especial.
    </p>
    <div class="text" style="margin-bottom: 30px">
      <ul>
        <li>Asesoría Personalizada</li>
        <li>Sastrería y Ajustes a Medida</li>
        <li>Estilismo Privado</li>
        <li>Experiencia de Compra VIP</li>
        <li>Selección de Regalos Personalizados</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServicesPage",
};
</script>

<style>
.center {
  text-align: center;
}

.text {
  margin: 0px 15% 0px 15%;
  line-height: 30px;
}

.row {
  margin: 0px 15% 0px 15%;
}

.row img {
  width: 20%;
  height: 20%;
  margin: 20px;
  margin-bottom: 90px;
  filter: grayscale();
}

.banner {
  background-image: url("https://images.pexels.com/photos/2463271/pexels-photo-2463271.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1");
  width: 100%;
  height: 300px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  margin-bottom: 20px;
  filter: grayscale();
}
</style>
