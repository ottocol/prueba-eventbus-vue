<template>
 <div class="componente1">
     <input type="text" v-model="texto"> 
     <button v-on:click="guardar">Enviar</button>
 </div>    
</template>

<script>
import {EventBus} from '../util/event-bus.js'

export default {
  name: 'Componente1',
  data: function() {
          return {
              texto:''
          }
  },
  methods: {
      guardar : function() {
          EventBus.$emit('send-data', this.texto);
      }
  }

}
</script>

<style>
    .componente1 {
        border: 1px solid red;
    } 
</style>
