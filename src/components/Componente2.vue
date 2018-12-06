<template>
 <div class="componente2">
    Datos recibidos: {{textoRecibido}}
 </div>    
</template>

<script>
import {EventBus} from '../util/event-bus.js'

export default {
  name: 'Componente2',
  data: function() {
          return {
              textoRecibido:''
          }
  },
  methods: {
      guardar : function() {
          console.log('guardar')
      }
  },
  created() {
    EventBus.$on('send-data', (data) => {
        this.textoRecibido = data
    });
  }

}
</script>


<style scoped>
    .componente2 {
        border: 1px solid blue;
    } 
</style>