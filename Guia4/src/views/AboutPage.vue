<template>
  <div class="about-page">
    <div class="banner"></div>
    <h1 class="center">Acerca de Nosotros</h1>
    <p class="text">
      Villalobos es sinónimo de lujo y exclusividad. Nuestra tienda ha sido
      cuidadosamente diseñada para ofrecer una experiencia única a quienes
      valoran la elegancia y el estilo. Con una selección curada de las marcas
      más prestigiosas a nivel mundial, nos dedicamos a satisfacer los gustos
      más exigentes. En Villalobos, no solo ofrecemos productos de alta calidad,
      sino también un servicio personalizado que garantiza que cada cliente
      disfrute de una atención inigualable. Nuestra pasión por el lujo y la
      excelencia nos ha consolidado como un referente en la moda y el buen
      gusto.
    </p>
    <div class="row">
      <img
        src="https://i.pinimg.com/564x/cd/5b/4a/cd5b4a4949f5c89f80fed4c7e804c3ac.jpg"
        alt=""
      />
      <img
        src="https://i.pinimg.com/564x/39/fe/13/39fe13325651965c113053b6bc63a7f8.jpg"
        alt=""
      />
      <img
        src="https://i.pinimg.com/564x/40/72/23/407223dddd331cfc1afa20aab207aea7.jpg"
        alt=""
      />
      <img
        src="https://i.pinimg.com/564x/de/8e/15/de8e158980ef1609f63b7719e4b3e412.jpg"
        alt=""
      />
    </div>
    <div class="center row" style="margin-top: 0px">
      <h2>Visítanos</h2>
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3876.6833034090205!2d-89.25713102581655!3d13.677011299022496!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8f632e2dc7b6e30f%3A0x9badf10fba0ea4ed!2sLa%20Gran%20Via!5e0!3m2!1sen!2ssv!4v1727374874264!5m2!1sen!2ssv"
        width="800"
        height="450"
        style="border: 0"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutPage",
};
</script>

<style scoped>
.center {
  text-align: center;
}

.text {
  margin: 0px 15% 0px 15%;
  line-height: 30px;
}

.row {
  margin: 0px 15% 20px 15%;
}

.row img {
  width: 20%;
  height: 20%;
  margin: 20px;
  filter: grayscale();
}

.banner {
  background-image: url("https://images.pexels.com/photos/5490969/pexels-photo-5490969.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1");
  width: 100%;
  height: 300px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  margin-bottom: 20px;
  filter: grayscale();
}
</style>
