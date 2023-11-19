<template>
  <div 
        class="contenedor-resultado">
        <h2>Cotización</h2>
        <div class="resultado">
          <img 
            :src="'https://cryptocompare.com' + cotizacion.IMAGEURL" 
            alt="imagen cryto">
          <div>
            <p>El precio es de: <span> {{ cotizacion.PRICE}} </span></p>
            <p>El precio más alto del dia: <span> {{ cotizacion.HIGHDAY}} </span></p>
            <p>El precio más bajo del dia: <span> {{ cotizacion.LOWDAY}} </span></p>
            <p>Variacion últimas 24h: <span> {{ cotizacion.CHANGEPCT24HOUR}}% </span></p>
            <p>Última actualización: <span> {{ cotizacion.LASTUPDATE}} </span></p>
          </div>
        </div>
      </div>
</template>

<script setup>
  defineProps({
    cotizacion: {
      type: Object,
      required: true,
    }
  });
</script>