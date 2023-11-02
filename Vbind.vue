<script setup>
import {ref} from 'vue'
const divid=ref('div01')
const textcolor=ref('Mindtree')
const content = ref('<b> LTI Mindtree </b>')
const status = ref(true)
const attr1 = ref('id')
const attr2 = ref('class')
const users=ref(0)
const cart =ref(['First item','Second item'])
const persons=ref([{id:1,name:"Vaidehi",city:"Pune"},{id:2,name:"Vaishnavi",city:"London"}])
const item = ref('')

function addItem(){
    cart.value.push('X')
}

function removeItem(){
    cart.value.pop()
}
</script>

<template>
    <select v-model="countries" multiple>
        <option value="IN">INDIA</option>
        <option value="US">UNITES STATES OF INDIA</option>
        <option value="UK">UNITED KINGDOM</option>
        <option value="UAE">UNITED ARAB EMIRATES</option>
    </select> {{ countries }} <br/>

    <input type="text" v-model="item"/> {{ item }}<br/>



    <ul>
        <li v-for= "(person,count) in persons"> {{ count+1 }}) {{ person.name }} is from {{ person.city}} </li>
    </ul>



    <button v-on:click="addItem()">Add</button>
    <button v-on:click="removeItem">Remove</button>
    <ul>
        <li v-for="(item,count) in cart">{{ count+1 }} {{ item }}</li>
    </ul>





    <button v-on:click="users++">Add</button>
    

    <h4 v-if ="users<=0"> No users </h4>
    <h4 v-else-if ="users==1">  One user</h4>
    <h4 v-else>{{ users }}</h4>

    




    <div  v-bind:[attr1]="divid" v-bind:[attr2]="textcolor" v-html ="content">
    
    </div>

    <div v-if="status">
        <p>If content</p>
    </div>

    <div v-show="status">
        show content 
    </div>
    
</template> 

<style>
.Mindtree{
    color:blueviolet
}</style>