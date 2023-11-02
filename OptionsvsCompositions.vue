<script setup>
import { onMounted, reactive, ref } from 'vue';

    
    const refObj = ref([{id:"10",name:"Vaidehi",city:"Mumbai"},{id:"11",name:"Raj",city:"Pune"}])
    const reactObj=reactive([{id:"9",name:"Pratik",city:"Jalgaon"},{id:"11",name:"Raj",city:"Pune"}])

    const username = ref('Vaidehi')
    function updateUsername(newUsername){
        username.value=newUsername
    }
    

    const isModalShown= ref( false )
    function showModal() {
        isModalShown.value = true
    }



    onMounted(() => {
        updateUsername('Vaidehi Joshi')
        
    })
    function change(){
        //refObj.value.id=5;
        //refObj.value.city="Pune"

       // reactObj.city="Pune"
        //reactObj.name="Soumya"

      
    

        
        
    }
    change()


    
       

  
</script>
<template>
    {{ refObj[0].name}}<br/>
    <!-- {{ refObj[1].name }} -->
    {{ reactObj[1].name }}
</template>