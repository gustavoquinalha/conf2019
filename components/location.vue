<template lang="html">
  <div class="content size margin" id="location">

    <div class="container wrap location align-center">
      <div class="flex-grow-1 flex-basis-300 ">
        <div class="box-title">
          <h2>
            LOCALIZAÇÃO DO EVENTO
          </h2>
        </div>

        <div class="header--block--date container column">
          <div class="box-data container column margin-bottom-40">
            <span class="span-uppercase">Localização</span>
            <span class="font-span">Parque Internacional de Exposições Francisco Feio Ribeiro - Maringá PR</span>
          </div>

          <div class="box-data container column margin-bottom-40">
            <span class="span-uppercase">DATA</span>
            <span class="font-span">28 de julho</span>
          </div>

          <div class="box-data container column">
            <router-link to="#tickets" class="btn btn-lg btn-primary btn-fit">
              Comprar tickets
            </router-link>
          </div>
        </div>
      </div>

      <div class="flex-grow-1 flex-basis-300">
        <div class="map-content">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d14644.417575241552!2d-51.9018197!3d-23.4205958!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xbfb7c9cce3800fc1!2sParque+Internacional+de+Exposi%C3%A7%C3%B5es+Francisco+Feio+Ribeiro!5e0!3m2!1spt-BR!2sbr!4v1524840886684"
            width="100%" height="400" frameborder="0" style="border:0" allowfullscreen></iframe>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.location {
  .map-content {
    margin-left: 100px;
    height: 400px;
    background: #ddd;
    margin-top: 50px;
    position: relative;
    @media screen and (max-width: 720px) {
      margin-left: 0;
    }

    &:after {
      content: "";
      width: 100%;
      height: 400px;
      position: absolute;
      bottom: -80px;
      left: -80px;
      z-index: -1;
      background-image: url("~/assets/images/map.svg");
      background-position: left bottom;
      background-repeat: no-repeat;
      background-size: contain;
    }
  }
}
.container-location {
  li {
    padding-right: 10px;
    &:last-child {
      padding-right: 0;
    }
  }
}

.header--block--date {
  .span-uppercase {
    font-size: 16px;
    font-weight: bold;
    margin-bottom: 16px;
    color: $color-1;
  }
  .font-span {
    line-height: 1.5;
    font-size: 24px;
  }
}
</style>
