<script setup>
import {ref} from 'vue'
const emp = ref(
    {
        FirstName:"",

        LastName:"",

        Country:"",

        MobileNumber:"",

        Email:""
    }
)

const status=ref(false)

function change_status()
{
    status.value=true
}
</script>
<template>
    
      <h1>Vue Form </h1>
      <h4>First Name</h4>    
      <input type="text" v-model="emp.FirstName" required>
      <h4>{{ FirstName }}</h4>

      <h4>Last Name</h4>    
      <input type="text" v-model="emp.LastName" required>
      <h4>{{ LastName }}</h4>

      <h4>Country</h4>    
      
        <select v-model="emp.Country">
        <option value="India">India</option>
        <option value="US">UNITES STATES OF INDIA</option>
        <option value="UK">UNITED KINGDOM</option>
        <option value="UAE">UNITED ARAB EMIRATES</option>
       
        
    </select> <br/><br>

        
    <h4>Mobile Number</h4>    
      <input type="text" v-model="emp.MobileNumber" required>
      <h4>{{ MobileNumber }}</h4>

      <h4>Email</h4>    
      <input type="text" v-model="emp.Email" required>
      <h4>{{ Email }}</h4>
  
        

       
       <button v-on:click="change_status">Submit</button>

       <p v-if="status">Form Submitted Successfully</p>
       <p v-if="status">Details : {{ emp }}</p>

        
        
    
    
  </template>

  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#visa {
  margin: 20px auto;
  max-width: 700px;
}
label{
  display: block;
  margin: 20px 0 10px;
}
input {
  font-size: 30px;
  border: 1px double rgb(102, 97, 96) ;
  border-radius: 4px;
}
button {
  font-size: 16px;
 background: rgb(64, 179, 140);
  padding: 0.4rem 1.3rem;
  text-align: center;
  border: none;
  cursor: pointer;
  border-radius: 4px;
 margin: 10px;
}
span{
  width: 30px;
  float: right;
  cursor: pointer;
}
span:hover{
  color: brown;
}
.previous{
  border: 1.5px solid;
  padding:5px;
  margin-bottom: 10px;
}
</style>