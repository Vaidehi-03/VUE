<script setup>
import {ref,computed} from 'vue'
import { userCartStore } from '../components/stores/cart.js';
const cartStore= userCartStore()

//const oddOrEven=computed(()=>{
    //if(count.value % 2==0)return 'even'
    //return 'odd'
//})


//const  oddOrEven=() => {
    //if(count.value%2==0)
    //
       // return "Even";
    //}
    //else
    //{
      //  return "Odd";
    //}
//}

</script>

<template>
    <div>
        {{  cartStore.count }}
    </div>
    <div>
        <button @click="cartStore.increaseCount">+</button>
        <button @click="cartStore.decreaseCount">-</button>

    </div>
    <div>
        This counter is : {{ cartStore.oddOrEven }}
    </div>
</template>