
<template>
  <div> Calculadora
   <p>PRIMER NUMERO : <input  v-model.number="numero1" /></p>
   <p>SEGUNDO NUMERO :  <input v-model.number="numero2"/> </p>
   <button @click="sumarnumeros">SUMAR</button>
   <h1>RESULTADO
    {{ suma }}
   </h1>
  </div>

</template>
 
 
 <script>
 import { ref } from 'vue'

 export default {
  setup(){
    const numero1 = ref ('')
    const numero2 = ref ('')
    const suma = ref ('')

    function sumarnumeros(){
      suma.value= numero1.value + numero2.value;

    }
    return{
      numero1,
      numero2,
      suma,
      sumarnumeros

    };
  },
 };
</script>


