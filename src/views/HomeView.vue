<template>
  <div>
    <div class="home">
      Hello
      <p ref="p">MY name is {{ person.name }} and my age is {{ person.age }}</p>
      <button @click="person.age++">Inc AGE</button>
      <button @click="handleClick" >Click me</button>
      <input type="text"  v-model="person.name">
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

import {ref,reactive} from 'vue'

export default {
  name: 'HomeView',
  setup(){
    console.log("setup");

    const p = ref(null);

    const person = reactive({name:"ravi", age:"29"})
    // let name  = ref("mario");
    // let age = ref(30);
    // let name  = "sahil";
    // let age = 49;

    const handleClick=()=>{
      person.name = 'sahil';
      person.age = '20';
      // name = "ravi"
      // age  = 90

    }
    

    return {person, handleClick, p }
  },

  data(){
    return{
    score:5,
    }
  },
  created(){
    console.log("created")
    
  },
  mounted(){
    console.log("mounted") 
  },
}
</script>
